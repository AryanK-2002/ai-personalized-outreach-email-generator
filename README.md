# AI Personalized Email Generator using n8n

## Overview

This project is an AI-powered personalized outreach email generator built using n8n, OpenRouter/OpenAI & LinkedIn profile data. The workflow automates the process of researching a prospect and generating a customized cold email tailored to their professional background, experience, and interests.

The goal of the project is to reduce the time spent on manual prospect research while improving the quality and personalization of outreach emails.

---

## Problem Statement

Writing personalized cold emails at scale is a time-consuming process. Sales teams, recruiters, founders & business development professionals often spend significant effort researching prospects before drafting outreach messages.

This workflow automates that process by:

* Collecting prospect information from LinkedIn
* Extracting relevant professional insights
* Generating highly personalized outreach emails using AI
* Producing structured output that can be directly used for email campaigns

---

## Features

* Automated LinkedIn profile data extraction
* AI-driven prospect analysis
* Dynamic prompt generation
* Personalized email creation
* Structured JSON output
* Fully automated workflow using n8n
* Easily customizable prompts
* Scalable architecture for outreach campaigns

---

## Tech Stack

### Workflow Automation

* n8n

### AI Model

* OpenRouter
* OpenAI GPT Models

### Data Collection

* Apify
* LinkedIn Profile Scraping

### API Integration

* HTTP Request Nodes
* JSON Parsing
* Custom Prompt Engineering

---

## Workflow Architecture

```text
LinkedIn Profile URL
          │
          ▼
      Apify Scraper
          │
          ▼
    Profile Data Extraction
          │
          ▼
    Data Cleaning & Formatting
          │
          ▼
    Prompt Construction
          │
          ▼
 OpenRouter / OpenAI API
          │
          ▼
 Personalized Email Generation
          │
          ▼
       JSON Output
```

---

## How It Works ?

### Step 1: Input

The workflow receives a LinkedIn profile URL of the target prospect.

### Step 2: Data Extraction

Apify extracts relevant information such as:

* Name
* Current role
* Company
* Professional experience
* Skills
* Summary
* Education
* Recent activities

### Step 3: Data Processing

The extracted information is cleaned and formatted into a structured format suitable for prompt generation.

### Step 4: Prompt Building

A dynamic prompt is created using the prospect's information and desired outreach objective.

### Step 5: AI Email Generation

The prompt is sent to OpenRouter/OpenAI, which generates a personalized cold email tailored specifically to the prospect.

### Step 6: Output

The workflow returns:

* Subject line
* Personalized email body
* Prospect insights
* Structured JSON response

---

## Example Use Cases

### Sales Outreach

Generate personalized prospecting emails for potential customers.

### Recruitment

Create customized messages for candidates based on their professional profiles.

### Founder Outreach

Reach out to investors, advisors, or industry experts with tailored communication.

### Business Development

Scale partnership and networking outreach efforts.

---

## Sample Output

### Subject

Exploring Opportunities at {{Company Name}}

### Email

Hi {{First Name}},

I came across your profile and was particularly interested in your experience in {{Industry/Domain}}.

Your work at {{Company Name}} and your background in {{Relevant Skill}} stood out to me.

I wanted to reach out because I believe there may be an opportunity for us to collaborate and exchange ideas that could create meaningful value.

Would you be open to a brief conversation sometime this week?

Looking forward to hearing from you.

Best regards,
{{Sender Name}}

---

## Challenges Faced

During development, several challenges were encountered:

* Handling inconsistent LinkedIn profile structures
* Managing API request limits
* Designing effective prompts for personalization
* Ensuring output consistency
* Reducing hallucinations in generated emails
* Improving response relevance

---

## Future Improvements

Planned enhancements include:

* CRM Integration (HubSpot, Salesforce)
* Google Sheets Integration
* Bulk Prospect Processing
* Automated Email Sending
* Lead Scoring
* Prospect Segmentation
* A/B Testing Support
* Follow-up Email Generation
* Analytics Dashboard
* Multi-channel Outreach Support

---

## Security Notice

All API credentials and authentication tokens have been removed from the public repository.

To run this workflow:

1. Add your own Apify API Token
2. Add your own OpenRouter/OpenAI API Key
3. Configure the required credentials inside n8n
4. Update node configurations if necessary

---

## Repository Structure

```text
personalized-email-generator-n8n/
│
├── README.md
├── workflow-public.json
│
├── screenshots/
│   ├── workflow-overview.png
│   └── sample-output.png
│
├── docs/
│   └── architecture.png
│
└── prompts/
    └── email-prompt.txt
```




