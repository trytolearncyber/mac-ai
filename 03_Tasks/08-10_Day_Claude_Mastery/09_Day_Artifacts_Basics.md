markdown
# Day 09: Artifacts Basics

## 📌 Goal

Artifact কি, কখন trigger হয়, এবং কিভাবে ব্যবহার করতে হয় তা বোঝা।

---

## 📝 Task 1: Artifact কি?

| প্রশ্ন | উত্তর |
|--------|-------|
| Artifact কি? | Claude-এর একটা **standalone output** যা আলাদা panel এ render হয় |
| Normal chat থেকে পার্থক্য | শুধু text না — usable, editable, interactive output |
| কেন special? | run করা যায়, edit করা যায়, reuse করা যায় |

---

### 📖 Real Life Example

**Normal Chat Response:**
> "BMI Calculator এর জন্য এই HTML code লিখতে পারেন..."

**Artifact Response:**
> একটা working BMI Calculator তৈরি করে দেয় → আপনি直接用 করতে পারেন

---

## 📝 Task 2: Artifact কখন Trigger হয়?

নিচের ধরনের কাজ বললে সাধারণত Artifact তৈরি হয়:

| # | Type | Example |
|---|------|---------|
| 1 | Code লিখতে বললে | "Python script বানাও" |
| 2 | Table বা report বানাতে বললে | "Sales report table" |
| 3 | Calculator বানাতে বললে | "BMI Calculator" |
| 4 | Form বানাতে বললে | "Contact form" |
| 5 | Dashboard বানাতে বললে | "Analytics dashboard" |
| 6 | HTML page তৈরি করতে বললে | "Landing page" |
| 7 | Diagram বানাতে বললে | "Network topology diagram" |

---

## 📝 Task 3: Artifact Types

| Type | Example | Use Case |
|------|---------|----------|
| **Code** | Python script, JS function | Automation, data processing |
| **HTML** | Web page, Form | Website, UI |
| **React** | Interactive component | Modern web app |
| **Markdown** | Notes, Report | Documentation |
| **SVG** | Diagram, Flowchart | Visual representation |

---

## 📝 Task 4: Example — BMI Calculator

### Prompt
একটা BMI Calculator বানাও



### Claude কী করে

| Step | Action |
|------|--------|
| 1 | HTML তৈরি করে |
| 2 | CSS styling দেয় |
| 3 | JavaScript calculation যোগ করে |
| 4 | Artifact panel এ render করে |

### Result
একটা usable mini app তৈরি হয়ে যায় — আপনি直接用 করতে পারেন।

---

## 📝 Task 5: Artifact কেন Powerful?

| Normal Chat | Artifact |
|-------------|----------|
| শুধু text | Usable output |
| Read only | Editable |
| Simple response | Interactive |
| Temporary | Reusable |
| পড়া যায় | ব্যবহার করা যায় |

> **এক কথায়:** Chat response → পড়া যায়, Artifact → ব্যবহার করা যায়

---

## 📝 Task 6: Artifact দিয়ে কি কি বানানো যায়?

| কাজ | Artifact Type | Use Case |
|-----|---------------|----------|
| Landing Page | HTML | Website |
| Dashboard | React | Analytics |
| BMI Calculator | HTML + JS | Health tool |
| Tic-Tac-Toe Game | React | Fun project |
| Sales Report | Markdown | Business |
| Flowchart | SVG | Process mapping |
| Resume | Markdown/HTML | Job application |
| Admin Panel | React + Tailwind | Internal tool |

---

## 📖 Real Life Example — Website

**Prompt:**
একটা modern landing page বানাও



**Result:** HTML/CSS Artifact → directly usable website

---

## 📖 Real Life Example — Dashboard

**Prompt:**
একটা sales dashboard বানাও



**Result:** React Artifact → interactive dashboard

---

## 📖 Real Life Example — Documentation

**Prompt:**
API documentation markdown এ বানাও



**Result:** Markdown Artifact → ready-to-use documentation

---

## 📖 Real Life Example — Diagram

**Prompt:**
Network topology diagram বানাও



**Result:** SVG Artifact → visual diagram

---

## 📝 Task 7: Quick Summary

| Feature | Normal Chat | Artifact |
|---------|-------------|----------|
| Format | Text only | Code/HTML/React/Markdown/SVG |
| Usability | Read only | Usable |
| Edit | ❌ | ✅ |
| Interactive | ❌ | ✅ |
| Reusable | ❌ | ✅ |

---

## 💡 Important Note

Artifact হলো:

- AI-generated workspace output
- Reusable component
- Editable project block

এটা future AI workflow এর অনেক বড় অংশ — বিশেষ করে n8n, Cursor, Claude, AI coding tools এ Artifact mindset খুব important।

---

## ⚠️ Common Mistakes

| ভুল | সঠিক |
|-----|-------|
| Artifact কে normal chat response মনে করা | Artifact আলাদা panel এ থাকে |
| Artifact edit করতে না জানা | Artifact可以直接 edit করা যায় |
| Complex task না দিয়ে simple task দেওয়া | Specific task দিলে ভালো output আসে |

---

## 🎯 Today's Goal Completed

- [x] Artifact কি বুঝেছি
- [x] কখন trigger হয় জানি
- [x] বিভিন্ন type চিনতে পারি
- [x] ব্যবহারিক উদাহরণ দেখেছি

---

## 📁 Log File

**Save to:** `05_Daily_Logs/09_Day_Log.md`

```markdown
# Day 09 Log

**Date:** 2026-06-14

## Checklist
- [x] Artifact কি বুঝেছি
- [x] কখন trigger হয় জানি
- [x] ৫টা type জানি
- [x] উদাহরণ দেখেছি

## Summary (One Line)
Artifact = standalone usable output (code/HTML/React) যা আলাদা panel এ render হয় এবং edit করা যায়।
🔖 Tags: #Day09 #Artifacts #Claude #MACMatrix


┌─────────────────────────────────────────────────────────────────────┐
│                      Day 09 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  Artifact = standalone output (code/HTML/React/Markdown/SVG)       │
│                                                                      │
│  Normal Chat → পড়া যায়                                            │
│  Artifact    → ব্যবহার করা যায় (run, edit, reuse)                  │
│                                                                      │
│  Trigger: code, table, calculator, form, dashboard বললে            │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
