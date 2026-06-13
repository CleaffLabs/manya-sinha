# AI Form Submission & QA AI Agent Workflows

## Overview
This repository contains two AI-powered workflows built using n8n:

* **AI Form Submission Workflow** – Collects user-submitted questions and answers, automatically generates relevant tags using AI, and stores the data in a database.
* **QA AI Agent Workflow** – Acts as a chatbot that searches the stored knowledge base and provides answers to user queries.

These workflows demonstrate the use of automation, AI models, data storage, and retrieval systems within n8n.

## Workflow 1: AI Form Submission

### Purpose
The AI Form Submission workflow is used to build a knowledge base from user-submitted content.

### Features
* Accepts form submissions
* Evaluates trust conditions
* Generates relevant tags using an AI model
* Stores questions, answers, and tags in a database/data table

### Workflow Structure
Form Submission → Conditional Check → AI Tag Generation → Database Storage

### Example
**Input:**
**Question:** What is encapsulation?

**Output:**
**Answer:** Encapsulation is the process of wrapping data and methods into a single unit, such as a class, and restricting direct access to that data using access modifiers. This is a fundamental concept in object-oriented programming, often referred to as data hiding.

**Tags:** encapsulation, oop, java, classes, access modifiers

**Stored Record:**
* Question
* Answer
* Tags

## Workflow 2: QA AI Agent

### Purpose
The QA AI Agent provides answers to users by searching the knowledge base created by the Form Submission workflow.

### Features
* Conversational chat interface
* AI-powered responses
* Database search tool integration
* Conversation memory support
* Knowledge retrieval from stored records

### Workflow Structure
Chat Trigger → AI Agent → Database Search Tool → Response Generation

### Example
**User Question:**
"What is encapsulation?"

**Agent Response:**
"Encapsulation is the process of wrapping data and methods into a single unit, such as a class, and restricting direct access to that data using access modifiers. This is a fundamental concept in object-oriented programming, often referred to as data hiding."

## Screenshots
**AI Form Submission Workflow**
<img width="1647" height="887" alt="image" src="https://github.com/user-attachments/assets/b3e21a61-4ede-4d1e-a508-bb68cc647c63" />

**QA AI Agent Workflow**
<img width="425" height="260" alt="image" src="https://github.com/user-attachments/assets/4f88f22b-b981-4e02-94c8-a64220ac0955" />

**Chatbot Demo**
<img width="1918" height="1023" alt="image" src="https://github.com/user-attachments/assets/ec2f0ec2-a9fd-457b-bfd6-11e3d4b20830" />

## How the Workflows Work Together
The Form Submission workflow populates the database with structured knowledge.
The QA AI Agent workflow uses the same database as its source of information.

**Flow:**
Form Submission Workflow
↓
Database / Data Table
↓
QA AI Agent Workflow

This allows new information submitted through forms to become searchable by the AI agent.

## Technologies Used
* n8n
* Google Gemini
* AI Agent Nodes
* Data Tables/ Database Storage
* Workflow Automation
* Chatbot Interface

## Notes
* The workflows were developed and tested locally using n8n.
* Credentials and API keys are not included in exported workflow files.
* The chatbot URL generated during local testing is only accessible while the local n8n instance is running.

## Files
* AI_form_submission.json
* QA_AI_agent.json
