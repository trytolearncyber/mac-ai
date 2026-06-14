markdown
# Day 12: Webhook কি? (Webhook What Is)

## 📌 Goal

Webhook কনসেপ্ট clearভাবে বোঝা এবং n8n এ এর basic usage understand করা।

---

## 📝 Task 1: Webhook কি?

| প্রশ্ন | উত্তর |
|--------|-------|
| Webhook কি? | "কিছু হলে আমাকে জানাও" system — কোনো event ঘটলে অন্য system নিজে থেকে notify করে |
| অন্য নাম | Reverse API, HTTP callback, web callback |

### সহজ ভাষায়

| API | Webhook |
|-----|---------|
| তুমি request পাঠাও | System নিজে notify করে |
| "এখন data দাও" | "কিছু ঘটেছে, জানানো হলো" |
| তুমি বারবার check করো | Event হলে auto জানায় |

---

## 📝 Task 2: API vs Webhook পার্থক্য

| বিষয় | API | Webhook |
|------|-----|----------|
| কে শুরু করে | Client (তুমি) | Server (system) |
| Data কবে আসে | যখন request করা হয় | Event ঘটলে |
| Process | Pull model | Push model |
| Resource use | বেশি (বারবার call লাগে) | কম (event-based) |
| Example | Weather API request | Payment success notification |

---

### 📖 Simple Analogy

| Situation | API | Webhook |
|-----------|-----|----------|
| Parcel tracking | তুমি গিয়ে জিজ্ঞেস করো "parcel এসেছে?" | দোকান নিজে call করে জানায় "parcel এসেছে!" |
| Restaurant order | তুমি গিয়ে জিজ্ঞেস করো "খাবার ready?" | Waiter নিজে বলে "খাবার ready" |
| Flight status | তুমি website এ check করো | Airline SMS পাঠায় "flight delayed" |

---

## 📝 Task 3: Real-Life Webhook Examples

| Service | Event | Action |
|---------|-------|--------|
| Stripe | Payment complete | Invoice generate |
| GitHub | Code push | Auto deploy |
| WooCommerce | New order | Email to warehouse |
| Facebook Forms | Form submit | CRM lead add |
| Calendly | Meeting booked | Google Calendar update |
| Gmail | New email | Slack notification |
| Typeform | Survey complete | Google Sheets save |

---

## 📝 Task 4: n8n এ Webhook কিভাবে কাজ করে

### Step-by-step

| Step | Action |
|------|--------|
| 1 | n8n এ নতুন workflow তৈরি করো |
| 2 | **Webhook Trigger node** add করো |
| 3 | একটি unique URL তৈরি হবে |
| 4 | এই URL অন্য system এ ব্যবহার করো |
| 5 | Event ঘটলেই সেই URL hit হবে |
| 6 | n8n workflow automatically execute হবে |

### Example URL
https://your-n8n.app.n8n.cloud/webhook/abc123

text

---

### Webhook Flow (Formula)
Event ঘটে
↓
Webhook URL এ POST request যায়
↓
n8n receive করে
↓
Workflow trigger হয়
↓
Action execute হয়

text

---

## 📝 Task 5: n8n এ কোন Node?

| Node | কখন ব্যবহার করবে |
|------|------------------|
| **HTTP Request Node** | API call করার জন্য (তুমি request পাঠাও) |
| **Webhook Trigger Node** | Event receive করার জন্য (system notify করে) |

---

## 📊 API vs Webhook: Quick Comparison

| Feature | API | Webhook |
|---------|-----|---------|
| Direction | Request → Response | Event → Notification |
| Initiator | Client | Server |
| Timing | When you ask | When event happens |
| n8n Node | HTTP Request | Webhook Trigger |

---

## ⚠️ Common Mistakes

| ভুল | সঠিক |
|-----|-------|
| Webhook আর API একই মনে করা | API = request করলে response, Webhook = event হলে notify |
| Webhook URL কে না দেওয়া | URL অন্য system এ give করতে হবে |
| সব কাজে Webhook ব্যবহার করা | যেখানে real-time দরকার না, সেখানে API sufficient |

---

## 🎯 Today's Goal Completed

- [x] Webhook কি বুঝেছি
- [x] API vs Webhook পার্থক্য জানি
- [x] রিয়েল লাইফ উদাহরণ জানি
- [x] n8n এ Webhook Trigger দেখেছি

---

## 📁 Log File

**Save to:** `05_Daily_Logs/12_Day_Log.md`

```markdown
# Day 12 Log

**Date:** 2026-06-14

## Checklist
- [x] Webhook কি বুঝেছি
- [x] API vs Webhook পার্থক্য জানি
- [x] ৬টা real-life উদাহরণ জানি
- [x] n8n Webhook Trigger দেখেছি

## Summary (One Line)
Webhook = event-based notification (server নিজে জানায়), API = request-based (client জিজ্ঞেস করে)
🔖 Tags: #Day12 #Webhook #APIvsWebhook #n8n #MACMatrix

text
┌─────────────────────────────────────────────────────────────────────┐
│                      Day 12 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  API     = "এখন data দাও" (তুমি request করো)                       │
│  Webhook = "কিছু হলে জানাবো" (system নিজে notify করে)              │
│                                                                      │
│  API → Pull model (বারবার check)                                    │
│  Webhook → Push model (event হলে auto)                              │
│                                                                      │
│  n8n: Webhook Trigger node = event receive করার জন্য                │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
