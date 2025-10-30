# ⚡ Lead Generation System  

An advanced, AI-powered **Lead Generation System** designed to automate and streamline your entire outreach workflow — from data collection to enrichment and personalized contact automation.  

This repository contains **three core agents**, each handling a different stage of the lead generation process:  
[1. **Lead Generation Agent**](https://github.com/mudassar-automation/Lead-Generation-Workflow/blob/main/Lead%20Generation%20Agent.json)  
[2. **Google Maps to Email Scraper (with Google Sheets Export)**](https://github.com/mudassar-automation/Lead-Generation-Workflow/blob/main/Google%20Maps%20to%20Email%20Scraper%20(with%20Google%20Sheets%20Export).json) 
[3. **LinkedIn Automation & Personalization (Lead Enrichment)**](https://github.com/mudassar-automation/Lead-Generation-Workflow/blob/main/LinkedIn%20Automation%20%26%20Personalization%20(Lead%20Enrichment).json)  

---

## 🧭 Overview  

This system automates the tedious parts of prospecting — finding, collecting, cleaning, enriching, and personalizing leads — so you can focus on closing deals and building real relationships.  

Each agent can run **independently** or **connect together** in a full workflow:
- Start with a Google Maps search to collect businesses and emails  
- Enrich those leads with AI-based context and industry data  
- Personalize and automate outreach through LinkedIn  

You can customize every stage to match your niche, target audience, or campaign style.

---

## ⚙️ Included Agents  

### 1️⃣ Lead Generation Agent  

## ⚙️ What This Workflow Does  

This automation triggers every time someone submits the **Lead Machine Form**. It then executes the following steps:

1. **Scrapes Business Data**  
   - Collects company name, website, phone, address, and category using **Apify** based on business type and location.  

2. **Extracts Email Addresses**  
   - Uses **Google Gemini AI** to extract and verify the best email from each business website.  

3. **Stores Leads in Google Sheets**  
   - Saves only valid leads with complete details.  

4. **Generates Cold Email Content**  
   - Creates personalized **subject lines** and **email bodies** using **AI**, matching your preferred tone (Friendly, Professional, Simple).  

5. **Sends Cold Emails via Gmail**  
   - Automatically sends the emails to each lead and logs results.  

6. **Updates Status in Google Sheets**  
   - Tracks sent status, timestamps, and outcomes for each contact.  

---

## 🧩 Setup  

To set up this workflow, you’ll need to configure each integration step:  

1. **Form Trigger**  
   - Customize the “Lead Machine” form fields (Business Type, Location, Lead Number, Email Style).  

2. **Apify API**  
   - Add your Apify Actor Endpoint URL in the HTTP Request node for data scraping.  

3. **Google Gemini**  
   - Add credentials for AI-based email extraction and validation.  

4. **Google Sheets**  
   - Connect your sheet for storing leads and email status.  

5. **OpenAI**  
   - Add your credentials for AI-based cold email generation.  

6. **Gmail**  
   - Connect your Gmail account to send personalized cold emails automatically.  

---

## 🛠️ How to Customize This Workflow  

You can easily tailor this system to match your goals and brand:  

- ✏️ **Change AI Email Prompts**  
  - Adjust the tone, structure, or message style to align with your brand voice or offer.  

- 🎯 **Add Filters**  
  - Only target leads that meet certain conditions (e.g., verified emails, active websites, specific industries).  

- 📊 **Modify Google Sheets Structure**  
  - Add custom columns like “Follow-up Date,” “Lead Source,” or “Email Status.”  

- 📬 **Switch Email Provider**  
  - Replace Gmail with another email provider or SMTP integration if needed.  

---

## 🚀 Outcome  

Once configured, this workflow becomes your **AI-powered Lead Machine** — finding businesses, extracting contacts, generating personalized cold emails, and sending them automatically while keeping everything tracked in one place.  

No manual scraping, no repetitive outreach — just **smart, scalable lead generation**.

➡️ [Click here to view the complete workflow code](https://github.com/mudassar-automation/Lead-Generation-Workflow/blob/main/Lead%20Generation%20Agent.json)
---

### 2️⃣ Google Maps to Email Scraper with Google Sheets Export 

# 🗺️ Google Maps Email Scraper System  

**Categories:** Lead Generation · Web Scraping · Business Automation  

This workflow creates a **completely free Google Maps email scraping system** that extracts unlimited business emails — without using expensive third-party APIs.  

Built entirely in **n8n** using simple HTTP requests and JavaScript, this system can generate **thousands of targeted leads** for any industry or location while operating at a **99% free cost structure**.

---

## 💡 Benefits  

- 💰 **Zero API Costs** — Operates entirely through free Google Maps scraping without expensive third-party services  
- ♾️ **Unlimited Lead Generation** — Extract emails from thousands of Google Maps listings across any industry  
- 🌍 **Geographic Targeting** — Search by specific cities, regions, or business types for precise lead targeting  
- ⚙️ **Complete Automation** — From search query to organized email list with minimal manual work  
- 🧹 **Built-in Data Cleaning** — Automatic duplicate removal, filtering, and data validation  
- 🚀 **Scalable Processing** — Handles hundreds of businesses per search with intelligent rate limiting  

---

## ⚙️ How It Works  

### 🔎 Google Maps Search Integration  
- Uses strategic **HTTP requests** to Google Maps search URLs  
- Processes queries like `"Calgary dentist"` or `"Miami lawyers"` to extract business listings  
- Bypasses API restrictions using **direct HTML scraping techniques**

### 🌐 Intelligent URL Extraction  
- Custom **JavaScript regex patterns** extract website URLs from Google Maps data  
- Filters out irrelevant domains (Google, schema, static files)  
- Returns a clean list of actual business websites for processing  

### 💻 Smart Website Processing  
- Loop-based architecture prevents IP blocking through **intelligent batching**  
- Built-in delays and redirect handling for reliability  
- Processes each website individually with error handling  

### ✉️ Email Pattern Recognition  
- Advanced **regex patterns** identify email addresses within website HTML  
- Extracts contact emails, info emails, and administrative addresses  
- Handles multiple email formats and validation patterns  

### 🧾 Data Aggregation & Cleaning  
- Automatically removes duplicate emails across all processed websites  
- Filters null entries and invalid formats  
- Exports clean, organized email lists directly to **Google Sheets**  

---

## 📄 Required Google Sheets Setup  

Create a Google Sheet with the following two tabs:

### **Search Tracking Sheet**  
| Column | Description |
|:--|:--|
| `searches` | Contains your search queries (e.g., `Calgary dentist`, `Miami lawyers`) |

### **Email Results Sheet**  
| Column | Description |
|:--|:--|
| `emails` | Contains extracted email addresses from all processed websites |

### 🧩 Setup Instructions  
1. Create a Google Sheet with two tabs: **"searches"** and **"emails"**  
2. Add your target search queries to the *searches* tab (one per row)  
3. Connect **Google Sheets OAuth credentials** in n8n  
4. Update your **Google Sheets Document ID** in all sheet nodes  

The workflow reads search queries from the first sheet and exports all extracted emails to the second sheet automatically.  

---

## 🏢 Business Use Cases  

- 🧰 **Local Service Providers** — Find competitors and potential partners in specific geographic areas  
- 💼 **B2B Sales Teams** — Generate targeted prospect lists for cold outreach campaigns  
- 🎯 **Marketing Agencies** — Build industry-specific lead databases for clients  
- 🏘️ **Real Estate Professionals** — Identify businesses in target neighborhoods for commercial outreach  
- 🏪 **Franchise Development** — Research potential markets and existing competition  
- 📊 **Market Research** — Analyze business density and contact info across regions  

---

## 💰 Revenue Potential  

This system transforms the economics of lead generation:  

- **$0 per lead** vs. **$2–$5 per lead** from paid databases  
- Process **1,000+ leads daily** without hitting API limits  
- Sell as a **done-for-you lead service** for **$500–$2,000 per industry or location**  
- Perfect for agencies offering local business lead generation  

---

## 🧠 Difficulty & Cost  

- **Difficulty Level:** Intermediate  
- **Estimated Build Time:** 1–2 hours  
- **Monthly Operating Cost:** **$0** (completely free)
  
---

## 🧩 Setup Steps  

### 1️⃣ Basic Workflow Architecture  
- Set up a **manual trigger** for testing and Google Sheets integration  
- Configure initial **HTTP Request node** for Google Maps searches  
- Enable SSL ignore and response headers for stable responses  

### 2️⃣ URL Extraction Code Setup  
- Add a **JavaScript code node** with custom regex patterns  
- Process input data from Google Maps HTML responses  
- Implement URL filtering to remove irrelevant domains  

### 3️⃣ Website Processing Pipeline  
- Add a **“Split in Batches”** node for intelligent looping  
- Configure HTTP requests with delays and redirect handling  
- Add error handling for non-scrapable sites  

### 4️⃣ Email Extraction System  
- Implement a **JavaScript code node** with email regex patterns  
- Validate email formats and handle multiple results per site  
- Aggregate all valid emails for export  

### 5️⃣ Data Cleaning & Export  
- Filter out null or duplicate entries  
- Use **“Split Out”** to merge all emails into one list  
- Connect **Google Sheets integration** for export  

### 6️⃣ Testing & Optimization  
- Use **Limit nodes** during testing to prevent IP blocks  
- Start small before scaling  
- Add **proxy integration** for higher volume scraping  

---

## ⚡ Advanced Optimizations  

Scale the system even further with:  

- **Multi-Page Scraping:** Scrape homepages and “Contact” pages for more emails  
- **Proxy Integration:** Add residential proxies for unlimited scraping  
- **Industry Templates:** Pre-configure searches by niche or industry  
- **Contact Data Expansion:** Extract phone numbers, addresses, and social media profiles  
- **CRM Integration:** Push leads directly to your CRM or sales pipeline  

---

## ⚠️ Important Considerations  

- 🕒 **Rate Limiting:** Built-in delays prevent IP blocking during normal use  
- 📈 **Scalability:** For heavy scraping, use proxies for higher throughput  
- ⚖️ **Compliance:** Always ensure proper data use and privacy compliance  
- ✅ **Data Quality:** Automated filters reduce noise, but manual checks are recommended for high-value campaigns  

---

## 🏁 Summary  

The **Google Maps Email Scraper System** is a cost-free, scalable solution for generating business leads with **zero paid APIs**.  
Whether you're a marketer, freelancer, or agency owner, this system gives you the ability to find and extract leads for any industry or location — fast, free, and fully automated.

➡️ [Click here to view the complete workflow code](https://github.com/mudassar-automation/Lead-Generation-Workflow/blob/main/Google%20Maps%20to%20Email%20Scraper%20(with%20Google%20Sheets%20Export).json) 
---

### 3️⃣ Lead Generation Automation on LinkedIn — Personalization & Enrichment  

# 💼 LinkedIn Lead Generation & Enrichment System  

This system automates **LinkedIn lead generation and enrichment** through a six-stage process that connects **Apollo.io**, **LinkedIn Data API**, and **Google Sheets** — providing verified emails, detailed profiles, and personalized outreach insights.  

---

## ⚙️ Workflow Summary  

This automation runs in **six clear stages**:

### 1️⃣ Lead Collection (via Apollo.io)  
- Automatically pulls leads based on **keywords, job roles, or industries** using Apollo’s API.  
- Captures essential data: **name, job title, company, LinkedIn profile URL, and Apollo User ID**.  
- Can be triggered through **form submission, webhook, WhatsApp, Telegram**, or any custom trigger that passes search parameters.  

---

### 2️⃣ LinkedIn Username Extraction  
- Extracts **usernames** from LinkedIn profile URLs using a lightweight script node.  
- These usernames are required for further enrichment through **RapidAPI (LinkedIn Data API)**.  

---

### 3️⃣ Email Retrieval (via Apollo.io User ID)  
- Fetches **verified work emails** using the Apollo User ID.  
- Adds a **double-verification layer** via **mails.so** — checking MX records and deliverability to remove invalid or inactive emails.  

---

### 4️⃣ Profile Summary (via LinkedIn API on RapidAPI)  
- Uses the **LinkedIn Data API** to enrich each lead with their **bio, summary, and headline**.  
- Helps you understand the lead’s expertise, company focus, and professional background.  

---

### 5️⃣ Activity Insights (Posts & Reposts)  
- Collects the lead’s **recent posts and reposts** to identify what they are currently engaging with.  
- Enables **personalized messaging** for outreach (e.g., referencing their latest post or shared topic).  

---

### 6️⃣ Leads Sheet Update  
- All enriched data is automatically written into a **Google Sheet**.  
- New columns are **added dynamically** without deleting existing information.  
- The sheet stays fully synced with status tracking (done / failed / pending).  

---

## 🔁 Smart Retry Logic  

Each workflow includes built-in **fail-safe retry logic** to maintain full data coverage:  

- Tracks status for every lead:  
  - ✅ **done** — processed successfully  
  - ❌ **failed** — issue occurred (auto-retry scheduled)  
  - ⏳ **pending** — waiting for next run  
- Failed rows are **automatically retried** after a custom delay (e.g., 2 weeks).  
- Guarantees minimal drop-offs and maximum completion.  

---

## 📊 Google Sheets Setup  

Make copies of these two template sheets:  

- **Template 1:** Apollo Leads Scraper & Enrichment  
- **Template 2:** Final Enriched Leads  

The system will append data (emails, bios, activities, etc.) step by step as enrichment progresses.

---

## 🔐 API Credentials Needed  

### 1️⃣ Apollo API  
- Sign up and generate your API key at the **[Apollo Developer Portal](https://apollo.io/developer)**.  
- Enable the **“Master API Key”** option so one key works across all endpoints.  

### 2️⃣ LinkedIn Data API (via RapidAPI)  
- Subscribe at **[RapidAPI – LinkedIn Data](https://rapidapi.com/)**.  
- Use your key in the `x-rapidapi-key` header field for enrichment requests.  

### 3️⃣ Mails.so API  
- Get your API key from your **[mails.so dashboard](https://mails.so)**.  
- Used for validating and filtering undeliverable or inactive email addresses.  

---

## 🛠️ Troubleshooting – LinkedIn Lead Machine  

### ✅ Common Mistakes & Fixes  

#### 1. API Keys Not Working  
- Ensure that all API keys (Apollo, RapidAPI, mails.so) are active and correct.  
- Apollo’s “Master API Key” must be **enabled**.  
- Keys should be saved as **Generic Credentials** inside n8n.  

#### 2. Leads Not Found  
- Broaden search queries — overly specific filters can return zero results.  
- Verify that Apollo is returning valid data for your search parameters.  

#### 3. LinkedIn URLs Missing or Invalid  
- Check that Apollo results include complete LinkedIn profile URLs.  
- Invalid or missing URLs will cause username extraction to fail.  

#### 4. Emails Not Coming Through  
- Apollo may not have verified emails for all leads.  
- mails.so may filter out invalid or expired addresses — review logs for details.  

#### 5. Google Sheet Not Updating  
- Ensure the Google Sheet is shared with the account connected to n8n.  
- Check for matching column headers and correct formatting (no merged cells).  

#### 6. Status Columns Not Changing  
- Each row must include a `done`, `failed`, or `pending` value.  
- Missing status fields will prevent retry logic from triggering.  

#### 7. RapidAPI Not Returning Data  
- Confirm that each lead has a valid LinkedIn username.  
- Check your RapidAPI subscription limits — ensure your plan is active.  

#### 8. Workflow Not Running  
- Verify that the trigger node (form, webhook, etc.) is **enabled**.  
- Confirm you’re passing all required input parameters (keyword, role, etc.).  

---

## 🚀 Outcome  

Once configured, this workflow becomes a **fully automated LinkedIn Lead Machine** — discovering new leads, verifying their emails, enriching their profiles, and organizing everything in Google Sheets for personalized outreach.  

You get **verified, enriched, and ready-to-contact leads** with minimal manual input — ideal for sales teams, agencies, and B2B marketers.

➡️ [Click here to view the complete workflow code](https://github.com/mudassar-automation/Lead-Generation-Workflow/blob/main/LinkedIn%20Automation%20%26%20Personalization%20(Lead%20Enrichment).json)  
---
