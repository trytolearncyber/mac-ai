# Day 08: Claude Models + Commands

## 📌 Goal

Claude interface এ confident হওয়া, সঠিক model বেছে নিতে পারা।

---

## 📝 Task 1: Claude Models — কোনটা কখন ব্যবহার করবে?

### Model Comparison

| Model | Speed | Best For | Cost |
|-------|-------|----------|------|
| **Haiku** | ⚡ Fastest | Simple tasks | Lowest |
| **Sonnet** | ⚡ Fast | Daily work | Medium |
| **Opus** | 🐢 Slow | Complex problems | Highest |

---

### কখন কোন Model ব্যবহার করবে?

| Model | Use Case | Example |
|-------|----------|---------|
| **Haiku** | Quick answer, summarize, translate | "API কি? ২ লাইনে বলো" |
| **Sonnet** | Coding, analysis, writing (এইটা default) | "n8n workflow বানাতে help করো" |
| **Opus** | Research, complex reasoning, hard problems | "RAG system এর limitation বিশ্লেষণ করো" |

---

### সহজ নিয়ম (Remember Rule)

| Task Type | → | Model |
|-----------|---|-------|
| Simple | → | Haiku |
| Normal | → | Sonnet |
| Hard | → | Opus |

---

## 📝 Task 2: Essential Commands

### Command List

| Command | কাজ | Example |
|---------|-----|---------|
| `/explain` | Concept বুঝিয়ে দাও | `/explain RAG কি?` |
| `/summarize` | লম্বা text ছোট করো | `/summarize` + [text] |
| `/rewrite` | আবার লিখে দাও | `/rewrite এই paragraph` |
| `/improve` | আরো ভালো করো | `/improve এই prompt` |
| `/shorten` | ছোট করো | `/shorten এই explanation` |
| `/answer` | Complete solution দাও | `/answer day 08` |

---

### Command ব্যবহারের নিয়ম

| Rule | Description |
|------|-------------|
| 1 | `/` (slash) দিয়ে start করো |
| 2 | command এর পরে task লিখো |
| 3 | এক লাইনেই লিখো |

---

### 📖 Real Life Example

**Scenario:** তুমি RAG concept বুঝতে চাও

| Step | What to do |
|------|-------------|
| 1 | Type: `/explain RAG কি এবং কিভাবে কাজ করে?` |
| 2 | Claude step by step explain করবে |
| 3 | আরো ভালোভাবে বুঝতে চাইলে: `/explain আরো সহজভাবে` |

---

## 📝 Task 3: Keyboard Shortcuts

| Shortcut | কাজ |
|----------|-----|
| `Ctrl + Enter` | Message পাঠানো |
| `Ctrl + K` | New chat |

---

## 📝 Task 4: Pricing & Plans

| Plan | Price | Features |
|------|-------|----------|
| **Free** | $0 | Basic access, limited messages |
| **Pro** | $20/month | More messages, all models |
| **Team** | $30/user/month | Team collaboration |

---

## ⚠️ Common Mistakes

| ভুল | সঠিক |
|-----|-------|
| সব কাজে Opus ব্যবহার করা | Sonnet ব্যবহার করো (cheaper + faster) |
| `/` ছাড়া command লেখা | `/` দিয়ে start করো |
| complex task এ Haiku ব্যবহার | Haiku simple task এর জন্য |

---

## 🎯 Today's Goal Completed

- [x] Claude models পার্থক্য বুঝেছি
- [x] কোন কাজে কোন model use করব জানি
- [x] Essential commands জানি
- [x] Keyboard shortcuts জানি
- [x] Pricing plans জানি

---

┌─────────────────────────────────────────────────────────────────────┐
│                      Day 08 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  Haiku  → Simple tasks (summarize, translate)                       │
│  Sonnet → Daily work (coding, writing) ← DEFAULT                    │
│  Opus   → Hard problems (research, complex reasoning)               │
│                                                                      │
│  Commands: /explain /summarize /rewrite /improve /shorten /answer   │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘



## 📁 Log File

**Save to:** `05_Daily_Logs/08_Day_Log.md`

```markdown
# Day 08 Log

**Date:** 2026-06-14

## Checklist
- [x] Haiku, Sonnet, Opus পার্থক্য বুঝেছি
- [x] ৬টা essential commands জানি
- [x] Keyboard shortcuts জানি
- [x] Pricing plans জানি

## Summary (One Line)
Haiku=simple, Sonnet=daily, Opus=hard — /explain, /summarize, /rewrite, /improve, /shorten, /answer