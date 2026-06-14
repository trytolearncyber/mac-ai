📄 Day 19 — n8n Prompt Testing
🎯 GOAL: ৩টা ভিন্ন prompt test করা এবং best prompt চিহ্নিত করা

📝 Task 1: ৩টা Prompt
Prompt 1 — Basic:
Analyze this log: %LINK-5-CHANGED: Interface Gi0/1, changed state to down
Prompt 2 — Structured:
You are a network engineer.
Analyze this Cisco log and tell me:
1. What happened?
2. What is the impact?
3. What should I do next?

Log: %LINK-5-CHANGED: Interface Gi0/1, changed state to down
Prompt 3 — Role + Context + Format (সেরা):
You are a senior Cisco network engineer.
A NOC alert just came in. Analyze the log below 
and respond in this exact format:

ISSUE: [one line summary]
SEVERITY: [Critical/High/Medium/Low]
IMPACT: [what is affected]
ROOT CAUSE: [possible reasons]
ACTION: [exact commands to run]

Log: %LINK-5-CHANGED: Interface Gi0/1, changed state to down

📝 Task 2: Output Analysis
CriteriaPrompt 1Prompt 2Prompt 3সমস্যা clearly বলেছে?❌✅✅Severity বলেছে?❌❌✅Command দিয়েছে?❌❌✅Structured output?❌✅✅Production ready?❌❌✅
কেন Prompt 3 সেরা:

Role দিয়েছো → Claude জানে সে কে
Context দিয়েছো → Claude জানে situation কী
Format দিয়েছো → Output predictable হয়


📝 Task 3: n8n এ Dynamic Prompt
Manual Trigger
      ↓
Set Node → log data set করো
      ↓
HTTP Request Node (Claude API)
      ↓
Set Node → output compare করো
n8n এ Dynamic Prompt:
You are a senior Cisco network engineer.
Analyze this log: {{ $json.log }}

Respond in this format:
ISSUE:
SEVERITY:
ACTION:

📝 Prompt Engineering — ৫টা Core Rule
RuleভুলসঠিকRole দাও"Analyze this""You are a network engineer. Analyze this"Context দাও"Fix it""This is a production router. Fix it"Format বলো"Tell me the issue""Respond in this format: ISSUE / ACTION"Specific হও"Check the log""Find the interface name and state"Constraint দাওকিছু বলো না"Respond in maximum 3 sentences"

🔧 Practice Exercise
নিচের ৩টা log এর জন্য Prompt 3 style এ prompt বানাও এবং n8n এ test করো:
Log 1 — MikroTik:
firewall,drop input from 203.0.113.5 to 192.168.1.1 port 8291
Log 2 — Linux:
Failed password for root from 45.33.32.156 port 22 ssh2
Log 3 — Fortinet:
date=2024-01-15 level=alert msg="SSH login failed" src=185.220.101.1

⚠️ Common Mistakes
ভুলসমস্যাসমাধানVague promptGeneric উত্তর আসেSpecific role + format দাওFormat না বলাOutput প্রতিবার আলাদাExact template দাওContext বাদWrong assumptionSituation explain করোStatic prompt n8n এসব log এ same{{ $json.log }} দিয়ে dynamic করো

📁 Log File
markdown# Day 19 Log

**Date:** 2026-06-15

## Checklist
- [ ] Task 1: ৩টা prompt তৈরি করলাম
- [ ] Task 2: Output compare করলাম
- [ ] Task 3: n8n এ dynamic prompt test করলাম
- [ ] Practice: ৩টা log এ Prompt 3 test করলাম

## Summary (One Line)
Prompt quality র্যাংকিং বুঝলাম — Role + Context + Format = সেরা output।
