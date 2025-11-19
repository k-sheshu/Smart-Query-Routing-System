# **Smart Query Routing System – Automated Student Query Handling Using n8n + LLM**

An end-to-end automation workflow built using **n8n**, **LLMs**, and **sentiment analysis** to intelligently manage and route student queries to the correct department—without any manual intervention.

## 🚀 **Project Overview**

Handling student queries manually can be slow, repetitive, and prone to misrouting.  
This project solves that by creating a **Smart Query Routing System** that:

- Reads student queries submitted through Google Forms  
- Detects how urgent the query is  
- Understands which category it belongs to  
- Maps the category to the correct department  
- Automatically emails the concerned HOD with formatted details  

Everything happens instantly and automatically.


## ⚙️ **Features**

### ✅ **1. Automated Query Collection**
Queries are collected from **Google Forms → Google Sheets**, and each new entry automatically triggers the n8n workflow.

### ✅ **2. Sentiment Analysis (Urgent/Normal)**
An AI model analyzes the student's query to determine if it is **Urgent** or **Normal**.

### ✅ **3. LLM-Based Category Classification**
The system identifies what type of issue the student is facing, such as:
- LMS Access  
- Payment Issue  
- Technical Doubt  
- Assignments  
- Room Allocation  
- Teaching Methodology  
- And more…

### ✅ **4. Category → Department Mapping**
A predefined mapping table links each category to:
- A **Department**
- A **Department Email**

### **Example Mapping Table**
| **Category** | **Department** | **Email** |
|--------------|----------------|-----------|
| WiFi Issue | IT Support | it_support@innomatics.in |
| Payment Issue | Accounts Department | accounts@innomatics.in |
| LMS Access | LMS Technical Support | lms_support@innomatics.in |
| Assignments | Training Department | training@innomatics.in |

### ✅ **5. Automated Email Delivery**
The workflow composes and sends a formatted email containing:
- Student Name  
- Enrollment ID  
- Branch  
- Sentiment (Urgent/Normal)  
- Category  
- Query Message  

Emails are sent instantly to the correct **HOD**.

## 🔧 **Workflow Architecture**
Google Form
→ Google Sheets Trigger
→ Sentiment Analysis
→ LLM Category Classifier
→ Category to Department Mapping
→ Switch Routing
→ Generate Email
→ Send Email to HOD

## 📩 **Example Email Output (Plain Text)**

**Subject:**  
Urgent Query - LMS Access (HYD_JNTU)

**Body:**
Dear LMS Technical Support,

A new student query has been received. Please find the details below:

Name: Vangapandu Lakshmi
Enrollment ID: DS2456
Branch: HYD_JNTU
Sentiment: Urgent
Category: LMS Access

Query:
"I can’t access my LMS account since yesterday."

Kindly look into this issue at the earliest.

Thank you,
Innomatics Query Routing System


## 🧠 **Why This Project Matters**

This automation proves that **technology doesn’t need to be complex to be impactful**.  
Even small, thoughtful workflows can save time, reduce workload, and improve communication.

## 📎 **Tech Stack**

- **n8n Automation**
- **Google Sheets**
- **Google Forms**
- **LLM (OpenAI / Gemini)**
- **Sentiment Analysis**
- **SMTP / Gmail Email Delivery**

## 💡 **Future Enhancements**

- Student confirmation email  
- Dashboard for query statistics  
- Priority escalation system  
- Multi-language support  

⭐ **If this project helped you, please consider giving the repository a star!**
