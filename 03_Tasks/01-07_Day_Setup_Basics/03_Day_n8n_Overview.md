# Day 03: n8n Overview – n8n কি? কেন শিখবো?

---

## 🎯 Goal

- n8n কি বুঝতে পারব
- n8n কখন ব্যবহার করব জানব
- n8n এর ভালো-খারাপ চিনতে পারব
- n8n.cloud এ ফ্রি সাইন আপ করতে পারব

---

## 📝 Task 1: n8n কি?

| প্রশ্ন | উত্তর |
|--------|-------|
| n8n কি | একটি **অটোমেশন টুল** যা বিভিন্ন app কে সংযুক্ত করে কাজ auto করে |
| টাইপ | **Low-code/No-code**, ওপেন সোর্স, ফ্রি |
| কি করা যায় | ইমেইল auto, সোশ্যাল মিডিয়া schedule, API call, AI workflow |

**📖 Real Life Example:**

> Gmail এ নতুন ইমেইল আসলে → Google Sheets এ save → Slack এ notification

---

## 📝 Task 2: কখন n8n ব্যবহার করবে?

### ✅ ব্যবহার করা উচিত

| # | পরিস্থিতি | কারণ |
|---|-----------|------|
| 1 | প্রতিদিন একই কাজ করতে হয় | সময় বাঁচায় |
| 2 | একাধিক tool connect করতে হয় | Gmail + Sheets + Slack |
| 3 | API call করতে হয় | Data fetch বা push |
| 4 | ফ্রি solution চাই | ওপেন সোর্স |
| 5 | নিজের মতো customize করতে চাই | কোড যোগ করা যায় |

### ❌ ব্যবহার করা উচিত না

| # | পরিস্থিতি | কারণ |
|---|-----------|------|
| 1 | non-technical team | setup একটু জটিল |
| 2 | খুব simple workflow | IFTTT/Zapier সহজ |
| 3 | real-time প্রয়োজন | n8n সামান্য lag দিতে পারে |
| 4 | enterprise team use | self-host maintain করতে হবে |

---

## 📝 Task 3: n8n এর ভালো-খারাপ

### ✅ Pros

| # | Pros |
|---|------|
| 1 | **ফ্রি এবং ওপেন সোর্স** – no monthly fee |
| 2 | **সেল্ফ-হোস্ট করা যায়** – data নিজের কাছে |
| 3 | **400+ integrations** – অনেক app support করে |
| 4 | **Visual builder** – code না লিখেও কাজ করে |
| 5 | **Code node** – 필요하면 JS লেখা যায় |

### ❌ Cons

| # | Cons |
|---|------|
| 1 | **Learning curve আছে** – সময় লাগবে |
| 2 | **Debug করা কঠিন** – ভুল খুঁজতে সময় যায় |
| 3 | **Self-host maintenance** – server manage করতে হবে |
| 4 | **Mobile UI ভালো না** – desktop প্রয়োজন |
| 5 | **Free plan limited** – 5,000 executions/month |

---

## 📝 Task 4: n8n.cloud সাইন আপ

### Step-by-step

| Step | Action |
|------|--------|
| 1 | https://n8n.cloud |
| 2 | "Sign Up" click |
| 3 | Email + Password দাও |
| 4 | Free plan select |
| 5 | Dashboard এ ঢুকো |

### Dashboard Menu

| Menu | কাজ |
|------|-----|
| **Workflows** | সব workflow এখানে, নতুন build করো |
| **Credentials** | API keys store করো (Claude, Google) |
| **Executions** | কবে কতবার run হয়েছে |
| **Settings** | Account settings |

✅ Sign up complete হলে check mark দাও → [x]

---

## 📝 Task 5: Dashboard Explore

### Dashboard এ যা দেখবে

| Item | Description |
|------|-------------|
| Workflows page | খালি থাকবে, নতুন build করো |
| + Create Workflow | নতুন start |
| Templates | ready-made workflow (later explore) |
| Credentials | ফাঁকা, পরে API key যোগ করো |

---

## 📖 Real-world Use Case

**Scenario:** ছোট ই-কমার্স দোকান

**Problem:** প্রতিদিন ৫০টি অর্ডার → manual email confirm → ২ ঘন্টা লাগে

**n8n Solution:**

| Step | Action |
|------|--------|
| Trigger | WooCommerce webhook (order created) |
| Action 1 | Customer কে email confirmation |
| Action 2 | Google Sheets এ order save |
| Action 3 | Telegram/Slack এ seller notify |

**Benefit:**

| Benefit | Result |
|---------|--------|
| সময় বাঁচে | ২ ঘন্টা → 0 |
| ভুল কমে | auto system |
| Customer satisfaction | instant confirmation |

---

## ⚠️ Common Mistakes

| ভুল | সঠিক |
|-----|-------|
| n8n আর Zapier একই মনে করা | n8n বেশি powerful |
| একদিনে সব শেখার চেষ্টা | daily practice |
| direct local setup শুরু | first cloud use |
| tutorial শুধু দেখা | নিজে try করা |

---

## 🎯 Today's Goal Completed

- [x] n8n কি explain করতে পারব
- [x] কখন n8n use করব বলতে পারব
- [x] n8n dashboard এ ঢুকতে পারব

---
┌─────────────────────────────────────────────────────────────────────┐
│                      Day 03 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  n8n = open source automation tool                                  │
│  Use when: repetitive work + multiple tools + need customization    │
│  Pros: free, self-host, 400+ integrations                           │
│  Cons: learning curve, debug hard, free plan limited                │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘


## 📁 Log File

**Save to:** `05_Daily_Logs/03_Day_Log.md`

```markdown
# Day 03 Log

**Date:** 2026-06-14

## Checklist
- [x] n8n কি বুঝেছি
- [x] কখন ব্যবহার করব জানি
- [x] pros and cons জানি
- [x] n8n.cloud sign up করেছি
- [x] dashboard explore করেছি

## Summary (One Line)
n8n হলো open source automation tool — free, visual builder, 400+ integrations.