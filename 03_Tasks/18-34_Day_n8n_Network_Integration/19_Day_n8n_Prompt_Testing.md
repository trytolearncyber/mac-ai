# 📄 Day 19 — n8n Prompt Testing
\\ Network Down Senerio : Network Down Real-World Troubleshooting for Network Engineers.md

## 🎯 Goal
৩টা ভিন্ন prompt test করে best prompt চিহ্নিত করা এবং prompt engineering শেখা।

---

# 📖 Story: MAX Prompt শেখার গল্প

MAX n8n শিখছে। সে Claude API ব্যবহার করে network log analyze করতে চায়। কিন্তু প্রথমবার prompt লিখে ভালো output পাচ্ছে না।

## ❓ MAX সমস্যা
> "কিভাবে prompt লিখলে Claude best উত্তর দেবে?"

আজ সে ৩টা different prompt test করে best prompt খুঁজে বের করবে।

---

# 📝 Task 1: ৩টা Prompt Test

---

## 🔴 Prompt 1 — Basic Prompt
### 🧠 MAX যা লিখলো
Analyze this log:
%LINK-5-CHANGED: Interface Gi0/1, changed state to down
---

### 🤖 Claude যা উত্তর দিলো

The log indicates that interface Gi0/1 has changed state to down.
---
### 😐 MAX Reaction: "এটা তো আমি নিজেও জানি! কোন severity? কি করতে হবে? কিছুই বললো না!"

---

### ❌ Problems
* No role
* No context
* No response format
* Generic answer

---

## 🟡 Prompt 2 — Structured Prompt
### 🧠 MAX যা লিখলো

You are a network engineer.
Analyze this Cisco log and tell me:

1. What happened?
2. What is the impact?
3. What should I do next?

Log:
%LINK-5-CHANGED: Interface Gi0/1, changed state to down

---

### 🤖 Claude যা উত্তর দিলো
What happened?
Interface Gi0/1 went down.

What is the impact?
Traffic on that interface is affected.

What should I do next?
Check physical connection and run:

show interfaces Gi0/1
---

### 🙂 MAX Reaction : "একটু ভালো। role দিয়েছি বলে উত্তর improve হয়েছে। কিন্তু severity বললো না।"

---

### ✅ Improvements
* Role added
* Questions added
* More structured output

---

### ❌ Missing
* Severity level নেই
* Multiple troubleshooting commands নেই
* Production-ready format না

---

## 🟢 Prompt 3 — Role + Context + Format
### 🧠 MAX যা লিখলো
You are a senior Cisco network engineer.
A NOC alert just came in.

Analyze the log below and respond in this exact format:

ISSUE: [one line summary]
SEVERITY: [Critical/High/Medium/Low]
IMPACT: [what is affected]
ROOT CAUSE: [possible reasons]
ACTION: [exact commands to run]

Log:
%LINK-5-CHANGED: Interface Gi0/1, changed state to down
---

### 🤖 Claude যা উত্তর দিলো
ISSUE:
Interface Gi0/1 has transitioned to down state

SEVERITY: High

IMPACT: Traffic traversing Gi0/1 is disrupted

ROOT CAUSE: Physical link failure, cable issue, or neighbor device shutdown

ACTION:
show interfaces Gi0/1
show logging | include Gi0/1
show cdp neighbors Gi0/1
Check physical cable and connection
---

### 😍 MAX Reaction : "এইটাই চাইছিলাম! severity, impact, root cause, এবং exact commands — সব পেয়েছি!"

---

## ✅ Why Prompt 3 Best
* Role clearly defined
* Real-world context provided
* Exact output format specified
* Actionable troubleshooting commands
* Production-ready response

---

# 📊 Task 2 — Prompt Comparison Table

| Criteria            | Prompt 1 | Prompt 2 | Prompt 3 |
| ------------------- | -------- | -------- | -------- |
| Problem identified  | ❌        | ✅        | ✅        |
| Severity included   | ❌        | ❌        | ✅        |
| Impact included     | ❌        | ✅        | ✅        |
| Root cause included | ❌        | ❌        | ✅        |
| Multiple commands   | ❌        | ❌        | ✅        |
| Production ready    | ❌        | ❌        | ✅        |

---

# 🏆 Winner: Prompt 3

## 💡 MAX যা শিখলো
Role + Context + Format = Best Output
---

# 📝 Task 3 — Dynamic Prompt in n8n
MAX প্রতিবার prompt manually edit করতে চায় না।
তাই সে dynamic prompt ব্যবহার করলো।

---

## 🔄 Workflow Structure
Manual Trigger
      ↓
Set Node
(log variable set)
      ↓
HTTP Request Node
(Claude API Call)
      ↓
Set Node
(Output Parse)

---

 ## 📌 Example Log Variable
log = "%LINK-5-CHANGED: Interface Gi0/1, changed state to down"

---

## 🧠 n8n Dynamic Prompt Template
You are a senior Cisco network engineer.
A NOC alert just came in.
Analyze this log:
Log: {{ $json.log }}
Respond in this exact format:
ISSUE: [one line summary]
SEVERITY: [Critical/High/Medium/Low]
IMPACT: [what is affected]
ROOT CAUSE: [possible reasons]
ACTION: [exact Cisco commands to run]

---

### 😎 MAX Comment

> "এখন যেকোনো log দিলেই structured output পাচ্ছি!"

---

# 📚 Prompt Engineering — ৫টা Golden Rule

| # | Rule               | ❌ Wrong           | ✅ Correct                     |
| - | ------------------ | ----------------- | -------------------------------- |
| 1 | Role দাও           | Analyze this log  | You are a senior Cisco engineer  |
| 2 | Context দাও        | Fix it            | A NOC alert just came in         |
| 3 | Format specify করো | Tell me the issue | Respond in ISSUE / ACTION format |
| 4 | Specific হও        | Check the log     | Find interface name and state    |
| 5 | Constraint দাও     | No limit          | Respond in maximum 50 words      |

---

# 🔧 Practice Exercise
## 🔹 Log 1 — MikroTik
firewall,drop input from 203.0.113.5 to 192.168.1.1 port 8291

### ✅ Prompt
You are a senior MikroTik network engineer.
A firewall alert just came in.
Analyze the log below and respond in this exact format:

ISSUE:
SEVERITY:
IMPACT:
ROOT CAUSE:
ACTION:

Log:
firewall,drop input from 203.0.113.5 to 192.168.1.1 port 8291

---

## 🔹 Log 2 — Linux
Failed password for root from 45.33.32.156 port 22 ssh2

### ✅ Prompt
You are a senior Linux system administrator.
An SSH security alert just came in.
Analyze the log below and respond in this exact format:

ISSUE:
SEVERITY:
IMPACT:
ROOT CAUSE:
ACTION:

Log:
Failed password for root from 45.33.32.156 port 22 ssh2
---

## 🔹 Log 3 — Fortinet
date=2024-01-15 level=alert msg="SSH login failed" src=185.220.101.1

### ✅ Prompt
You are a senior Fortinet security engineer.
A security alert just came in.
Analyze the log below and respond in this exact format:

ISSUE:
SEVERITY:
IMPACT:
ROOT CAUSE:
ACTION:

Log:
date=2024-01-15 level=alert msg="SSH login failed" src=185.220.101.1

---



# ⚠️ Common Mistakes & Fixes

| Mistake          | Problem                | Fix                   |
| ---------------- | ---------------------- | --------------------- |
| Analyze this log | Generic answer         | Add role + context    |
| No format        | Random output          | Define exact template |
| No context       | Wrong assumptions      | Explain the situation |
| Static prompt    | Same answer every time | Use `{{ $json.log }}` |

---



Example:

# 📊 HR + IT + AI Engineer Prompt Library (With Examples)

---

## 👥 HR Role

### 🧾 Task 1: Salary Issue

**Example Input:**
Salary not received this month

**Prompt:**
You are an HR assistant. Handle this request and respond professionally.

Issue:
Salary not received this month

**Output Type:**
Email / HR response

---

### 🧾 Task 2: Employee Complaint Summary

**Example Input:**
No promotion for 2 years, feeling ignored

**Prompt:**
You are an HR officer. Summarize this complaint and suggest action.

Message:
No promotion for 2 years, feeling ignored

**Output Type:**
Summary + action plan

---

## 💻 IT Role

### 🛠 Task 1: Password Reset

**Example Input:**
Cannot login to system

**Prompt:**
You are an IT support engineer. Provide step-by-step solution.

Problem:
Cannot login to system

**Output Type:**
Troubleshooting steps

---

### 🛠 Task 2: Printer Issue

**Example Input:**
Printer not printing documents

**Prompt:**
You are an IT helpdesk engineer. Analyze the issue and provide solution steps.

Issue:
Printer not printing documents

**Output Type:**
Issue + solution

---

## 🤖 AI Engineer Role

### 🧠 Task 1: Improve Prompt

**Example Input:**
Analyze this data

**Prompt:**
You are an AI prompt engineer. Improve this prompt for better AI results.

Prompt:
Analyze this data

**Output Type:**
Better optimized prompt

---

### ⚙️ Task 2: Automation Idea

**Example Input:**
Send email when new lead comes from website

**Prompt:**
You are an AI automation engineer. Suggest a workflow for this task.

Task:
Send email when new lead comes from website

**Output Type:**
Workflow design

---

### 🧩 Task 3: Classify Request

**Example Input:**
Build chatbot for customer support

**Prompt:**
You are an AI system designer. Classify this task and suggest solution.

Task:
Build chatbot for customer support

**Output Type:**
Category + solution approach

---

## 🧠 Key Understanding

- HR → people + salary + complaints  
- IT → systems + troubleshooting + support  
- AI Engineer → prompts + automation + design  

---

## 🎯 Golden Rule

Role + Real Problem + Clear Instruction = Best AI Output

---

## 🚀 Reusable Template

You can use this anytime:

You are a [ROLE].

Task:
<your problem>

Respond with:
- Clear explanation
- Step-by-step solution
- Actionable output





# 📁 Save Your Daily Log
## File Path
05_Daily_Logs/19_Day_Log.md

---



# 📌 Quick Reference Card

┌──────────────────────────────────────────────┐
│          PROMPT ENGINEERING CHEAT SHEET     │
├──────────────────────────────────────────────┤
│                                              │
│ ❌ BAD PROMPT                               │
│ Analyze this log                             │
│                                              │
│ ✅ GOOD PROMPT                              │
│ You are a senior engineer.                  │
│ A NOC alert just came in.                  │
│ Respond in ISSUE / SEVERITY / ACTION format │
│                                              │
├──────────────────────────────────────────────┤
│                                              │
│ 5 GOLDEN RULES                              │
│                                              │
│ 1️⃣ Role                                    │
│ 2️⃣ Context                                 │
│ 3️⃣ Format                                  │
│ 4️⃣ Specific                                │
│ 5️⃣ Constraint                              │
│                                              │
├──────────────────────────────────────────────┤
│                                              │
│ 🏆 WINNER: Prompt 3                         │
│                                              │
└──────────────────────────────────────────────┘
---


# 🔖 Tags
#Day19
#PromptTesting
#n8n
#PromptEngineering
#NetworkAutomation
#MACMatrix
---

