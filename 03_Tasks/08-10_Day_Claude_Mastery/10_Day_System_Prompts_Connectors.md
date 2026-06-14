# Day 10: System Prompts & Connectors

## 📌 Goal

Claude নিজের মতো customize করা, external tools connect করা।

---

## 📝 Task 1: System Prompt কি?

| প্রশ্ন | উত্তর |
|--------|-------|
| System Prompt কি? | Claude-এর "hidden instruction layer" যা conversation শুরু হওয়ার আগেই সেট করা থাকে |
| User দেখতে পায়? | না |
| কাজ কি? | পুরো behavior control করে |

> **সহজভাবে:** System Prompt = AI কিভাবে behave করবে তার rulebook

---

### Formula
System Prompt = Role + Language + Style + Constraints



---

## 📝 Task 2: নিজের জন্য System Prompt লিখো

### Breakdown

| Element | কি দিবে |
|---------|---------|
| **Role** | AI Automation শেখার mentor |
| **Language** | সব সময় বাংলা |
| **Style** | Bullet points, step-by-step, real-life examples, mistake ধরিয়ে দেওয়া |
| **Constraints** | একসাথে বেশি topic নয়, beginner friendly, motivational tone নয় |

---

### ✅ Ready to Use System Prompt
তুমি MAC Matrix এর AI Automation শেখার mentor।

Role: Expert AI Automation Teacher

Language: সবসময় বাংলায় উত্তর দাও

Style:

Bullet points এ explain করো

Step-by-step শেখাও

Real-life example ব্যবহার করো

ভুল হলে সেটি পরিষ্কারভাবে ধরিয়ে দাও

Constraints:

একসাথে অনেক topic cover করো না

Beginner friendly রাখো

Motivational tone ব্যবহার করো না

"তোমাকে" শব্দ ব্যবহার করো না



---

## 📝 Task 3: System Prompt কেন গুরুত্বপূর্ণ?

| Without System Prompt | With System Prompt |
|----------------------|---------------------|
| Random উত্তর দেয় | নির্দিষ্ট behavior follow করে |
| Style consistent থাকে না | Output stable হয় |
| Predictable নয় | Professional workflow তৈরি হয় |

---

## 📝 Task 4: Guardrails কি?

Guardrails হলো **safety + behavior rules** যা AI কে বলে "কি করা যাবে না"

### Example Guardrails

| Rule | Purpose |
|------|---------|
| Code ছাড়া উত্তর দিও না | Code focus |
| শুধু AI Automation বিষয়েই কথা বলো | Topic focus |
| শুধু বাংলা ভাষায় উত্তর দাও | Language focus |
| sensitive content avoid করো | Safety |

---

### System Prompt vs Guardrails

| System Prompt | Guardrails |
|---------------|------------|
| AI কেমন হবে | AI কী করতে পারবে না |
| Role define করে | Limit define করে |
| Behavior shape করে | Behavior control করে |

---

## 📝 Task 5: Connectors কি?

Connectors হলো Claude-এর **external tools integration**

> Claude শুধু chat না — বাইরের system এর সাথে connect করতে পারে

### Connector কী করতে পারে?

| Connector | কাজ |
|-----------|-----|
| **Google Drive** | File access |
| **GitHub** | Code repository access |
| **Notion** | Notes পড়া/লেখা |
| **Slack** | Messages read করা |

### Availability

| Plan | Connectors |
|------|------------|
| Free | ❌ No |
| Pro | ✅ Available |

---

## 📝 Task 6: Connectors কেন useful?

| Without Connector | With Connector |
|-------------------|----------------|
| "এই file summarize করো" → user কে copy paste করতে হয় | AI directly Google Drive file read করে summary দেয় |
| শুধু information | actual work system |

---

## 📖 Real Life Example

**Without Connector:**
> User: "Google Drive এ আমার resume আছে, summarize করো" → AI পারে না

**With Connector:**
> User: "Google Drive এ আমার resume আছে, summarize করো" → AI direct access করে summary দেয়

---

## 📝 Task 7: Google Drive Connector Setup (Pro Plan)

### Steps

| Step | Action |
|------|--------|
| 1 | Claude.ai → Settings |
| 2 | Connectors → Google Drive |
| 3 | Connect Google Account |
| 4 | Allow permissions |
| 5 | Done ✅ |

---

## 💡 Key Insight

| Component | মানে |
|-----------|------|
| **System Prompt** | AI brain setup |
| **Guardrails** | AI safety rules |
| **Connectors** | AI external hands |

---

## 📊 Quick Summary

| Topic | Definition |
|-------|------------|
| System Prompt | AI behavior define করে |
| Guardrails | AI limitation set করে |
| Connectors | AI external tools access দেয় |

---

## ⚠️ Common Mistakes

| ভুল | সঠিক |
|-----|-------|
| System Prompt না দেওয়া | System Prompt দিলে output stable হয় |
| Guardrails ignore করা | Guardrails safety এর জন্য জরুরি |
| Free plan এ connector আশা করা | Pro plan needed |

---

## 🎯 Today's Goal Completed

- [x] System Prompt কি বুঝেছি
- [x] নিজের system prompt লিখেছি
- [x] Guardrails কি জানি
- [x] Connectors কি বুঝেছি
- [x] Google Drive connector সম্পর্কে জানি (Pro plan needed)

---

## 📁 Log File

**Save to:** `05_Daily_Logs/10_Day_Log.md`

```markdown
# Day 10 Log

**Date:** 2026-06-14

## Checklist
- [x] System Prompt কি বুঝেছি
- [x] নিজের system prompt লিখেছি
- [x] Guardrails কি জানি
- [x] Connectors কি বুঝেছি
- [x] Google Drive connector জানি

## Summary (One Line)
System Prompt = behavior rulebook, Guardrails = safety rules, Connectors = external tools access
🔖 Tags: #Day10 #SystemPrompts #Guardrails #Connectors #MACMatrix


┌─────────────────────────────────────────────────────────────────────┐
│                      Day 10 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  System Prompt = Role + Language + Style + Constraints             │
│  Guardrails    = Safety + Behavior rules                            │
│  Connectors    = Google Drive, GitHub, Notion, Slack                │
│                                                                      │
│  Formula: System Prompt + Guardrails + Connectors = Perfect AI Setup│
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
