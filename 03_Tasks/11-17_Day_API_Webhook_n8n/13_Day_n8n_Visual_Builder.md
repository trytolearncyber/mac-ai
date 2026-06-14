markdown
# Day 13: n8n Visual Builder

## 📌 Goal

n8n ইন্টারফেসের সাথে পরিচিতি — dashboard চেনা, node বুঝা, প্রথম workflow তৈরি করা।

---

## 📝 Task 1: n8n.cloud ওপেন করো

| Step | Action |
|------|--------|
| 1 | https://n8n.cloud |
| 2 | Login করো |
| 3 | Dashboard এ ঢুকো |

---

## 📝 Task 2: Dashboard এর প্রতিটি অংশ চিনো

### n8n Dashboard Menu

| Menu | কাজ |
|------|-----|
| **Workflows** | সব workflow এর list (এখান থেকে open/edit করবে) |
| **Canvas** | Node সাজানোর জায়গা (workflow বানানোর জায়গা) |
| **Executions** | কতবার run হয়েছে, success/failed দেখাবে |
| **Credentials** | API keys সংরক্ষণ করো (Claude, Google, GitHub) |
| **Settings** | Account ও plan settings |

---

## 📝 Task 3: Claude কে জিজ্ঞেস করো — "n8n এর node কিভাবে কাজ করে?"

### নোড কি?

| প্রশ্ন | উত্তর |
|--------|-------|
| Node কি? | Workflow এর একটা ধাপ |
| কিভাবে কাজ করে? | প্রতিটি node একটা নির্দিষ্ট কাজ করে |
| কিভাবে connect করে? | Arrow দিয়ে connect করতে হয় |
| Data flow | Left থেকে right এ data flow করে |

---

### Node এর ৩ ধরন

| ধরন | কাজ | উদাহরণ |
|------|-----|---------|
| **Trigger** | Workflow শুরু করে | Webhook, Schedule, Email Trigger |
| **Action** | কাজ করে | HTTP Request, Claude API, Gmail |
| **Logic** | সিদ্ধান্ত নেয় | IF, Switch, Merge |

---

### Node Flow Example
Schedule Trigger ( শুরু )
↓
HTTP Request ( API call )
↓
IF Node ( condition check )
├─ YES → Gmail ( email পাঠাও )
└─ NO → Google Sheets ( log save )

text

---

## 📝 Task 4: প্রথমবার n8n খুললে যা করবে

| Step | Action |
|------|--------|
| 1 | **+ New Workflow** click করো |
| 2 | Canvas এ **+ button** click করো |
| 3 | **Schedule Trigger** খোঁজো |
| 4 | Drag করে canvas এ রাখো (বা click করে add করো) |
| 5 | **Save** করো |

---

## 🎯 Today's Goal Completed

- [x] n8n dashboard open করেছি
- [x] Dashboard এর menu গুলো চিনেছি
- [x] Node কি এবং কিভাবে কাজ করে জানি
- [x] ৩ ধরনের node চিনতে পারি
- [x] প্রথম workflow তৈরি করেছি (Schedule Trigger add)

---

## 📁 Log File

**Save to:** `05_Daily_Logs/13_Day_Log.md`

```markdown
# Day 13 Log

**Date:** 2026-06-14

## Checklist
- [x] n8n dashboard open করেছি
- [x] Workflows, Canvas, Executions, Credentials, Settings চিনেছি
- [x] Node = workflow এর ধাপ বুঝেছি
- [x] Trigger, Action, Logic node চিনতে পারি
- [x] প্রথম workflow তৈরি করেছি

## Summary (One Line)
n8n dashboard menu: Workflows, Canvas, Executions, Credentials, Settings — Node ৩ ধরন: Trigger, Action, Logic
🔖 Tags: #Day13 #n8n #VisualBuilder #Nodes #MACMatrix

text
┌─────────────────────────────────────────────────────────────────────┐
│                      Day 13 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  n8n Dashboard Menu:                                                │
│  ├─ Workflows   → workflow list                                     │
│  ├─ Canvas      → node সাজানোর জায়গা                               │
│  ├─ Executions  → run history                                       │
│  ├─ Credentials → API keys store                                    │
│  └─ Settings    → account settings                                  │
│                                                                      │
│  Node ৩ ধরন: Trigger (start) → Action (work) → Logic (decision)    │
│                                                                      │
│  Done: First workflow created (Schedule Trigger)                    │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
