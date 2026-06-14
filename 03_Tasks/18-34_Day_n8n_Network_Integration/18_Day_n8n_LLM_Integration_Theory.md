# 📄 Day 18 — n8n + LLM Integration Theory

**📁 Folder:** `03_Tasks/18-34_Day_n8n_Network_Integration/`
**📁 Log File:** `05_Daily_Logs/18_Day_Log.md`
**🎯 GOAL:** n8n এ Claude AI যোগ করার theory সম্পূর্ণ বোঝা

---

## 📝 Task 1: LLM কী এবং n8n এ কীভাবে কাজ করে

### LLM কী?
- LLM = Large Language Model
- উদাহরণ: Claude, ChatGPT, Gemini
- এটা text input নেয় → process করে → text output দেয়

### n8n এ LLM এর role:
- n8n একটা **workflow tool** — data move করে
- LLM একটা **brain** — data বোঝে এবং সিদ্ধান্ত নেয়
- দুটো মিলে = **Intelligent Automation**

### Basic Flow:
```
Data Source → n8n → LLM (Claude) → Action
```

### Real Example (তোমার network background দিয়ে):
```
Cisco Router Log আসলো
        ↓
   n8n সেটা receive করলো
        ↓
   Claude কে পাঠালো: "এই log এ কী সমস্যা?"
        ↓
   Claude বললো: "GigabitEthernet0/1 down — cable check করো"
        ↓
   Telegram এ alert গেলো
```

---

## 📝 Task 2: Claude API Theory

### API কীভাবে কাজ করে:
- Claude API = Claude এর সাথে program দিয়ে কথা বলার রাস্তা
- তুমি → Request পাঠাও → Claude → Response দেয়

### Request এর ৩টা মূল অংশ:

| অংশ | কী করে | উদাহরণ |
|-----|--------|---------|
| **API Key** | পরিচয় দেয় | `sk-ant-api...` |
| **Model** | কোন Claude | `claude-sonnet-4-6` |
| **Message** | কী জিজ্ঞেস করছো | `"এই log এ কী সমস্যা?"` |

### n8n এ Claude API ব্যবহারের ২টা উপায়:

**উপায় ১ — Built-in Claude Node (সহজ):**
```
n8n এ "Anthropic" node আছে
→ API Key দাও
→ Prompt লিখো
→ Done
```

**উপায় ২ — HTTP Request Node (flexible):**
```
HTTP Request Node
→ URL: https://api.anthropic.com/v1/messages
→ Method: POST
→ Headers: x-api-key, anthropic-version
→ Body: model, messages
```

### Claude API Key কোথায় পাবে:
- console.anthropic.com → Login → API Keys → Create Key

---

## 📝 Task 3: Network Log Analysis — AI Use Case

### কেন Network Log এ AI দরকার?

- একটা Cisco switch প্রতিদিন **হাজারো log** generate করে
- মানুষের পক্ষে সব পড়া সম্ভব না
- Claude এক সেকেন্ডে পুরো log পড়ে সমস্যা বের করে

### ৩টা Real Use Case:

**Use Case 1 — Cisco Log Analysis:**
```
Input:  "%OSPF-5-ADJCHG: Process 1, Nbr 10.0.0.2 on Gi0/1 from FULL to DOWN"
Output: "OSPF neighbor down। Interface বা cable সমস্যা হতে পারে।
         পরীক্ষা করো: show ip ospf neighbor"
```

**Use Case 2 — MikroTik Firewall Log:**
```
Input:  "firewall,drop input from 192.168.1.100 to 192.168.10.1 port 8291"
Output: "কেউ WAN থেকে WinBox access করার চেষ্টা করছে।
         IP 192.168.1.100 block করো।"
```

**Use Case 3 — Linux Server Log:**
```
Input:  "Failed password for root from 45.33.32.156 port 22 ssh2 (10 times)"
Output: "Brute force attack চলছে। fail2ban চালু করো অথবা
         IP 45.33.32.156 block করো।"
```

### n8n Workflow Design:
```
Schedule Trigger (প্রতি ঘণ্টায়)
        ↓
Execute Command Node (log file পড়ো)
        ↓
Claude Node (log analyze করো)
        ↓
IF Node (সমস্যা আছে কি না)
        ↓
Telegram/Email Alert
```

---

## 🔧 Practice Exercise

n8n তে এই simple workflow বানাও:

```
Manual Trigger
     ↓
Set Node (নিচের data set করো)
     {
       "log": "%LINK-5-CHANGED: Interface Gi0/1, changed state to down"
     }
     ↓
HTTP Request Node (Claude API call)
     ↓
Set Node (response থেকে শুধু text বের করো)
```

**HTTP Request Node Config:**
```
Method: POST
URL: https://api.anthropic.com/v1/messages
Headers:
  x-api-key: তোমার API key
  anthropic-version: 2023-06-01
  content-type: application/json

Body (JSON):
{
  "model": "claude-sonnet-4-6",
  "max_tokens": 500,
  "messages": [
    {
      "role": "user",
      "content": "Analyze this Cisco log: {{ $json.log }}"
    }
  ]
}
```

**Expected Output:**
```json
{
  "content": [
    {
      "text": "Interface GigabitEthernet0/1 is down. Check cable or connected device..."
    }
  ]
}
```

---

## ⚠️ Common Mistakes

| ভুল | কেন সমস্যা | সমাধান |
|-----|-----------|--------|
| API Key সরাসরি workflow এ লেখা | Security risk | n8n Credentials এ save করো |
| Response থেকে text বের না করা | পুরো JSON আসবে | `{{ $json.content[0].text }}` use করো |
| Model name ভুল লেখা | API error আসবে | `claude-sonnet-4-6` exactly লিখতে হবে |
| anthropic-version header বাদ দেওয়া | 400 error আসবে | সবসময় add করতে হবে |

---

## 📁 Log File: 18_Day_Log.md

```markdown
# Day 18 Log

**Date:** 2026-06-15

## Checklist
- [ ] Task 1: LLM concept বুঝলাম
- [ ] Task 2: Claude API theory বুঝলাম
- [ ] Task 3: Network Log Analysis use case বুঝলাম
- [ ] Practice: HTTP Request Node দিয়ে Claude call করলাম

## Summary (One Line)
n8n এ Claude API integrate করার theory এবং network log analysis use case সম্পন্ন।
```

---

**🎯 Day 18 Complete হলে Day 19 তে যাবো: Prompt Testing**



