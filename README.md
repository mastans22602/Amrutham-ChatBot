# 🍽️ Amrutham AI Restaurant Chatbot

An **AI-powered multilingual restaurant chatbot** built with **n8n** and **Google Gemini** for **Amrutham Indisches Restaurant**.

The chatbot acts as a virtual restaurant assistant that helps customers get quick answers about the restaurant, menu, opening hours, vegetarian options, reservations, takeaway services, and other general queries.

## ✨ Features

* 🤖 AI-powered conversational chatbot
* 🇬🇧 English language support
* 🇩🇪 German language support
* 🍽️ Menu and dish-related FAQs
* 💰 Menu price enquiries
* 🕐 Opening hours
* 📍 Restaurant location
* 🥗 Vegetarian and vegan options
* 🌶️ Food-related questions
* 🪑 Table reservation enquiries
* 🛍️ Takeaway information
* 🚚 Delivery information
* 📞 Restaurant contact information
* 💬 Conversational memory
* 🛡️ Anti-hallucination instructions
* 🌐 Designed for website integration

## 🏗️ Architecture

```text
                    Customer
                       │
                       ▼
              ┌─────────────────┐
              │ Restaurant      │
              │ Chatbot         │
              └────────┬────────┘
                       │
                       ▼
                ┌─────────────┐
                │ n8n Chat    │
                │ Trigger     │
                └──────┬──────┘
                       │
                       ▼
                ┌─────────────┐
                │ n8n AI      │
                │ Agent       │
                └──────┬──────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Google Gemini   │
              │ Chat Model      │
              └────────┬────────┘
                       │
                       ▼
             Restaurant Knowledge
                       │
                       ▼
                 AI Response
                       │
                       ▼
                    Customer
```

## 🛠️ Tech Stack

| Technology              | Purpose                                                |
| ----------------------- | ------------------------------------------------------ |
| **n8n**                 | Workflow automation and AI orchestration               |
| **Google Gemini**       | Natural-language understanding and response generation |
| **n8n AI Agent**        | Conversational AI logic                                |
| **n8n Chat Trigger**    | Receives customer messages                             |
| **Conversation Memory** | Maintains conversation context                         |
| **Website Chat Widget** | Customer-facing chatbot interface                      |

## 💡 Example Questions

Customers can ask questions such as:

### English

```text
What are your opening hours?

Where is the restaurant located?

What vegetarian dishes do you have?

Do you have vegan food?

Can I reserve a table?

Do you offer takeaway?

What is the price of Chicken Tikka Masala?
```

### German

```text
Wie sind Ihre Öffnungszeiten?

Wo befindet sich das Restaurant?

Welche vegetarischen Gerichte haben Sie?

Haben Sie vegane Gerichte?

Kann ich einen Tisch reservieren?

Bieten Sie Takeaway an?

Wie viel kostet Chicken Tikka Masala?
```

The chatbot automatically responds in the **same language as the customer**.

## 🧠 AI Behavior

The chatbot is designed to provide reliable restaurant information while minimizing incorrect answers.

It follows these principles:

* Uses verified restaurant information
* Does not invent menu items
* Does not guess prices
* Does not guess opening hours
* Does not falsely confirm reservations
* Handles unknown questions gracefully
* Advises customers to contact restaurant staff for allergy confirmation
* Responds politely and conversationally

If information is unavailable, the chatbot directs the customer to contact the restaurant.

## 🪑 Reservation Handling

The chatbot can collect reservation details such as:

* Customer name
* Date
* Time
* Number of guests

The current version **does not automatically confirm reservations**.

A future version can connect the chatbot to a real reservation/availability system through n8n.

## 🌐 Website Integration

The chatbot is designed to be embedded into the restaurant website using the n8n Chat Trigger.

Basic flow:

```text
Amrutham Website
       ↓
Chat Widget
       ↓
n8n Chat Trigger
       ↓
AI Agent
       ↓
Google Gemini
       ↓
Restaurant Information
       ↓
Customer Response
```

## 🚀 Future Improvements

Planned enhancements include:

* 🔎 RAG-based menu search
* 📄 Menu PDF ingestion
* 🗄️ Supabase / PostgreSQL integration
* 🪑 Real-time reservation availability
* 📱 WhatsApp integration
* 📞 Voice AI assistant
* 👨‍💼 Human handoff
* 📊 Customer analytics dashboard
* 🧾 Order-status enquiries
* 🎯 Customer lead collection
* 🌍 Additional language support

## 📂 Project Structure

```text
amrutham-restaurant-chatbot/
│
├── n8n/
│   └── amrutham-chatbot-workflow.json
│
├── knowledge/
│   └── restaurant-information.md
│
├── docs/
│   └── n8n-setup.md
│
├── .env.example
│
└── README.md
```

## ⚙️ Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/amrutham-restaurant-chatbot.git
cd amrutham-restaurant-chatbot
```

### 2. Import the n8n workflow

Open n8n and import:

```text
n8n/amrutham-chatbot-workflow.json
```

### 3. Configure Google Gemini

Add your Google Gemini API credentials to the Gemini Chat Model node.

**Never commit API keys or credentials to GitHub.**

### 4. Add restaurant information

Update the restaurant knowledge with verified information such as:

```text
Restaurant name
Address
Phone number
Opening hours
Menu
Menu prices
Vegetarian options
Vegan options
Takeaway
Delivery
Reservations
Parking
Payment methods
```

### 5. Activate the workflow

After testing the chatbot, activate the n8n workflow and configure the website chat integration.

## 🔐 Security

Sensitive credentials should never be stored in the GitHub repository.

Use environment variables or n8n credentials for:

* API keys
* AI provider credentials
* Database credentials
* Authentication tokens
* Private webhook configuration

## 🎯 Project Objective

This project demonstrates how **AI + workflow automation** can be used to create practical customer-service solutions for restaurants.

The project combines:

**AI + n8n + Google Gemini + Conversational Automation**

to create a multilingual virtual restaurant assistant that can operate 24/7.

## 👨‍💻 Author

**Shaik Mastan Vali**

UI/UX Designer → AI Workflow Automation & n8n

### Project

**Amrutham AI Restaurant Chatbot**

Built with ❤️ using **n8n and Google Gemini**.
