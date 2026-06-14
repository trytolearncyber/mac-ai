# 📊 Excel Data Analysis with Claude — Step-by-Step Guide

Excel data analyze, clean, visualize, এবং automate করার জন্য একটি complete workflow।

---

# ধাপ ১: Excel File Upload করুন

প্রথমে Excel বা CSV file Claude-এ upload করতে হবে।

এটি হতে পারে:

* Sales report
* School result sheet
* Financial হিসাব
* Survey data
* Inventory report
* যেকোন structured spreadsheet

## কীভাবে Upload করবেন

1. Claude open করুন
2. Attachment / Paperclip icon এ click করুন
3. Excel বা CSV file select করুন
4. Upload করুন

Claude automatically spreadsheet structure এবং columns বুঝে নেবে।

---

# ধাপ ২: Data Analyze করুন

ডেটার ভিতরে কী আছে এবং overall pattern কী, সেটা আগে বুঝতে হবে।

## Prompt

```text id="0p4rwm"
Act as a senior business analyst. Analyze this uploaded spreadsheet thoroughly.

Please explain:
- What this dataset represents and its overall structure
- Key trends or patterns over time or categories
- Any anomalies, spikes, or unusual data behavior
- Missing values or inconsistencies that require attention

Provide a structured summary with bullet points.
```

---

# ধাপ ৩: Data Clean + Fix করুন

Spreadsheet এ সাধারণত duplicate data, formatting issue, বা missing value থাকে।

Claude ব্যবহার করে এগুলো খুব দ্রুত identify করা যায়।

## Prompt

```text id="3ncf4z"
Act as a professional data cleaning specialist. Review this spreadsheet and identify any data quality issues.

Specifically look for:
- Duplicate rows or redundant records
- Inconsistent formatting (dates, currency, text vs numbers)
- Missing values or blank cells
- Outliers that may skew analysis

Please provide:
- A clear issue list
- Step-by-step Excel instructions to clean and fix each problem
```

---

# ধাপ ৪: Excel Formula Automatically Generate করুন

Complex formula মুখস্থ না রেখেও Claude দিয়ে formula generate করা যায়।

## Prompt

```text id="z1m4kk"
Act as an advanced Excel expert. Based on the columns in this spreadsheet, generate the exact Excel formulas needed for:

- Growth rate calculations
- Average and maximum values
- Lookup formulas (XLOOKUP or INDEX-MATCH)
- Conditional logic using IF or nested IF

For each formula:
- Include exact cell references
- Explain step-by-step how to apply it
```

---

# ধাপ ৫: Charts + Dashboard Idea Generate করুন

Data visualization করলে report অনেক বেশি understandable হয়।

## Prompt

```text id="d4tm9y"
Suggest the best visual charts and dashboard layout for this dataset.

For each recommendation provide:
- Ideal chart type
- X-axis and Y-axis setup
- Key insight the chart highlights
- Executive takeaway from the visual

Also suggest a clean dashboard structure.
```

---

# ধাপ ৬: Business Insights বের করুন

Claude-কে একজন business consultant এর মতো ব্যবহার করে important decision insight বের করা যায়।

## Prompt

```text id="m7x8qs"
Act as a senior growth consultant analyzing this spreadsheet.

Please identify:
- Top 3 growth opportunities
- Biggest risks or red flags
- Customer behavior patterns
- Product performance trends
- Actionable recommendations to improve efficiency or revenue

Write in a professional and easy-to-understand strategic advisory tone.
```

---

# ধাপ ৭: Automation Workflow তৈরি করুন

একই কাজ প্রতিদিন manually না করে automated reporting system তৈরি করা বেশি efficient।

## Prompt

```text id="6fg4tu"
Design a structured automated reporting workflow using this spreadsheet.

Please include:
- Weekly or monthly report ideas
- KPIs to track automatically
- Conditional formatting alerts
- Automation ideas using:
  - Power Query
  - Excel Macros
  - Integrations
  - Scheduled reporting

Explain the workflow step-by-step.
```

---

# ধাপ ৮: Executive Summary তৈরি করুন

সব analysis শেষে short professional summary তৈরি করুন।

## Prompt

```text id="u6nv1r"
Imagine you are presenting these findings to executives who only have 2 minutes to read.

Summarize the spreadsheet using:

- Current State
- Key Findings
- Strategic Recommendations

Keep it:
- Concise
- Professional
- Data-driven
- Easy to understand
```

---

# ✅ Recommended Workflow Order

1. Upload file
2. Analyze data
3. Clean the data
4. Generate formulas
5. Create charts & dashboard
6. Extract business insights
7. Build automation workflow
8. Create executive summary

---

# 🎯 Best Use Cases

এই workflow বিশেষভাবে useful:

* Sales analysis
* School বা university project
* Finance tracking
* Inventory management
* HR reporting
* Customer analytics
* Small business dashboard
* Operations reporting

---

# 🚀 Final Tip

Claude সবচেয়ে ভালো result দেয় যখন:

* Column names clear থাকে
* Data properly structured থাকে
* Specific প্রশ্ন করা হয়
* Updated dataset ব্যবহার করা হয়

Spreadsheet যত organized হবে, analysis তত accurate এবং useful হবে।
