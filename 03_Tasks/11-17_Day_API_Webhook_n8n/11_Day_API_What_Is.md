# Day 11: API কি? (API What Is)

## 📌 Goal

API কনসেপ্ট বোঝা — কিভাবে কাজ করে, কেন দরকার, এবং n8n এ কোথায় লাগবে।

---

## 📝 Task 1: API কি?

| প্রশ্ন | উত্তর |
|--------|-------|
| API কি? | Application Programming Interface — দুইটা system এর মধ্যে কথা বলার নিয়ম |
| সহজ ভাষায় | রেস্টুরেন্টের waiter — তুমি order দাও, waiter রান্নাঘরে নিয়ে যায়, খাবার নিয়ে আসে |

### Formula
Client → Request → API → Server → Response → Client

text

---

### API এর ৪টি ধাপ

| ধাপ | কি হয় | উদাহরণ |
|------|--------|---------|
| 1 | Request | "আমাকে weather দাও" |
| 2 | Receive | Weather server request পায় |
| 3 | Process | Database থেকে খোঁজে |
| 4 | Response | JSON format এ data ফেরত দেয় |

---

## 📝 Task 2: Real-Life উদাহরণ

| উদাহরণ | কোন API |
|---------|---------|
| Weather app এ temperature দেখা | Weather API |
| Google Maps এ location খোঁজা | Maps API |
| Bkash দিয়ে payment করা | Payment API |
| n8n থেকে Gmail পাঠানো | Gmail API |
| Facebook দিয়ে login করা | OAuth API |
| n8n + Claude AI কথা বলা | Anthropic API |

---

## 📝 Task 3: API Request এর ধরন (Methods)

| Method | কাজ | উদাহরণ |
|--------|-----|---------|
| **GET** | Data নিয়ে আসো | User list দেখাও |
| **POST** | নতুন data পাঠাও | নতুন user তৈরি করো |
| **PUT** | Data update করো | Name পরিবর্তন করো |
| **DELETE** | Data মুছে দাও | User delete করো |

---

## 📝 Task 4: JSONPlaceholder Practice

> URL: https://jsonplaceholder.typicode.com

### Browser এ এই links গুলো open করো

| Link | কি দেখবে |
|------|----------|
| https://jsonplaceholder.typicode.com/users | সব user list |
| https://jsonplaceholder.typicode.com/users/1 | 1 নাম্বার user |
| https://jsonplaceholder.typicode.com/posts | সব post |
| https://jsonplaceholder.typicode.com/posts/1 | 1 নাম্বার post |

### Response Example

```json
{
  "id": 1,
  "name": "Leanne Graham",
  "email": "Sincere@april.biz",
  "phone": "1-770-736-0988"
}
📝 Task 5: n8n এ API কিভাবে লাগবে?
Step	Action
1	HTTP Request node দিয়ে API call করা যায়
2	Response থেকে data নিয়ে next node এ পাঠানো যায়
3	Day 12 এ practice করবো (হাতে-কলমে)
📖 Real Life Example (Complete Flow)
text
তুমি Weather app open করলে
        ↓
App API request পাঠায় (GET https://api.weather.com/dhaka)
        ↓
Weather server data খুঁজে বের করে
        ↓
API response পাঠায় ({"temp": 32, "condition": "sunny"})
        ↓
App temperature দেখায়
📊 API Methods Summary
Method	কাজ	HTTP Code Success
GET	Read data	200 OK
POST	Create data	201 Created
PUT	Update data	200 OK
DELETE	Delete data	204 No Content
⚠️ Common Mistakes
ভুল	সঠিক
API আর Webhook একই মনে করা	API = request করলে response দেয়, Webhook = event হলে notify করে
সব request এ POST ব্যবহার করা	GET → read, POST → create, PUT → update, DELETE → delete
API key না দেওয়া	অনেক API এর authentication প্রয়োজন
🎯 Today's Goal Completed
API কি বুঝেছি

রিয়েল লাইফ উদাহরণ জানি

৪টি HTTP method জানি

JSONPlaceholder explore করেছি

📁 Log File
Save to: 05_Daily_Logs/11_Day_Log.md

markdown
# Day 11 Log

**Date:** 2026-06-14

## Checklist
- [x] API কি বুঝেছি
- [x] রিয়েল লাইফ উদাহরণ জানি
- [x] ৪টি HTTP method জানি
- [x] JSONPlaceholder explore করেছি

## Summary (One Line)
API = two systems talking (GET/POST/PUT/DELETE), n8n uses HTTP Request node for API calls.
🔖 Tags: #Day11 #API #HTTPMethods #JSONPlaceholder #MACMatrix

text
┌─────────────────────────────────────────────────────────────────────┐
│                      Day 11 Complete ✅                              │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  API = Client → Request → API → Server → Response → Client         │
│                                                                      │
│  GET    → Read data                                                  │
│  POST   → Create data                                                │
│  PUT    → Update data                                                │
│  DELETE → Delete data                                                │
│                                                                      │
│  Practice: JSONPlaceholder (fake API for testing)                   │
│  n8n use: HTTP Request node                                          │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
