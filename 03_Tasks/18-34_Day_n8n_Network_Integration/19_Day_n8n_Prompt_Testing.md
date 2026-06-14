📄 Day 19 — n8n Prompt Testing
🎯 GOAL: ৩টা ভিন্ন prompt test করা এবং best prompt চিহ্নিত করা

📝 Task 1: ৩টা Prompt তৈরি করো
একই Cisco log এর জন্য ৩টা আলাদা style এর prompt:
Prompt 1 — Basic (খুব সাধারণ):
Analyze this log: %LINK-5-CHANGED: Interface Gi0/1, changed state to down
Prompt 2 — Structured (ভালো):
You are a network engineer.
Analyze this Cisco log and tell me:
1. What happened?
2. What is the impact?
3. What should I do next?

Log: %LINK-5-CHANGED: Interface Gi0/1, changed state to down
Prompt 3 — Role + Context + Output Format (সেরা):
You are a senior Cisco network engineer.
A NOC alert just came in. Analyze the log below and respond in this exact format:

ISSUE: [one line summary]
SEVERITY: [Critical/High/Medium/Low]
IMPACT: [what is affected]
ROOT CAUSE: [possible reasons]
ACTION: [exact commands to run]

Log: %LINK-5-CHANGED: Interface Gi0/1, changed state to down

📝 Task 2: Output Analysis
প্রতিটা prompt এর output এই criteria দিয়ে judge করো:
CriteriaPrompt 1Prompt 2Prompt 3সমস্যা clearly বলেছে?❌✅✅Severity বলেছে?❌❌✅Command দিয়েছে?❌❌✅Structured output?❌✅✅Production ready?❌❌✅
Result: Prompt 3 সবসময় জিতবে কারণ:

Role দিয়েছো → Claude জানে কে সে
Context দিয়েছো → Claude জানে situation কী
Format দিয়েছো → Output predictable হয়


📝 Task 3: n8n এ Prompt Test করার উপায়
n8n Workflow:
Manual Trigger
      ↓
Set Node → log data set করো
      ↓
Claude Node (Prompt 1 দিয়ে run করো)
      ↓
Set Node (output save করো)

--- আবার same workflow ---

Claude Node (Prompt 3 দিয়ে run করো)
      ↓
দুটো output compare করো
n8n এ Dynamic Prompt লেখার নিয়ম:
You are a senior Cisco network engineer.
Analyze this log: {{ $json.log }}

Respond in this format:
ISSUE: 
SEVERITY: 
ACTION:

📝 Prompt Engineering — ৫টা Core Rule
RuleভুলসঠিকRole দাও"Analyze this""You are a network engineer. Analyze this"Context দাও"Fix it""This is a production router. Fix it"Format বলো"Tell me the issue""Respond in this format: ISSUE / ACTION"Specific হও"Check the log""Find the interface name and state from this log"Constraint দাওকিছু বলো না"Respond in maximum 3 sentences"

🔧 Practice Exercise
নিচের ৩টা log এর জন্য Prompt 3 style এ prompt বানাও এবং n8n এ test করো:
Log 1 — MikroTik:
firewall,drop input from 203.0.113.5 to 192.168.1.1 port 8291
Log 2 — Linux:
Failed password for root from 45.33.32.156 port 22 ssh2
Log 3 — Fortinet:
date=2024-01-15 level=alert msg="SSH login failed" src=185.220.101.1
Expected: প্রতিটা log এর জন্য Claude যেন বলে — কী হয়েছে, কতটা গুরুতর, এবং কী করতে হবে।

⚠️ Common Mistakes
ভুলসমস্যাসমাধানVague prompt দেওয়াGeneric উত্তর আসেSpecific role + format দাওFormat না বলাOutput প্রতিবার আলাদা হয়Exact format template দাওContext বাদ দেওয়াClaude wrong assumption করেSituation explain করোn8n এ static promptসব log এ same prompt{{ $json.log }} দিয়ে dynamic করো