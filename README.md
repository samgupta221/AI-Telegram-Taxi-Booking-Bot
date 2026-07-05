# 🚖 AI-Powered Telegram Taxi Booking Bot

An intelligent Taxi Booking Assistant built using **n8n**, **Telegram Bot API**, **Groq AI**, and **Google Sheets**.

The bot allows users to book taxis, check availability, answer FAQs, and automatically store bookings without any manual intervention.

---

## 📌 Features

- 🤖 AI-powered conversation using Groq LLM
- 🚖 Book taxis directly from Telegram
- 📋 Check taxi availability
- ❓ Answer Frequently Asked Questions
- 📝 Automatically store bookings in Google Sheets
- 💬 Interactive conversational booking flow
- ⚡ No-code automation using n8n
- 📊 Real-time order management

---

## 🏗️ Workflow Architecture

```
Telegram User
      │
      ▼
Telegram Trigger
      │
      ▼
AI Agent (Groq)
      │
 ┌────┼───────────────┐
 │    │               │
 ▼    ▼               ▼
FAQ Sheet      Taxi Details Sheet
 │
 ▼
Orders Sheet (Append Booking)
 │
 ▼
Telegram Response
```

---

## 🛠️ Tech Stack

- n8n
- Telegram Bot API
- Groq Chat Model
- Google Sheets API
- AI Agent
- Workflow Automation

---

## 📂 Google Sheets Used

### 🚖 Taxi_Details

Stores:

- Taxi Name
- Available Quantity
- Vehicle Type

Example

| Taxi | Available |
|------|-----------|
| WagonR | 2 |
| Swift Dzire | 5 |
| Maruti Ertiga | 7 |
| Tata Nexon EV | 4 |

---

### ❓ FAQ Sheet

Contains common customer queries.

Example

| Question | Answer |
|----------|--------|
| Cancellation Policy | Booking can be cancelled before pickup |
| Payment | Cash & Online supported |
| Booking Time | 24×7 Available |

---

### 📋 Orders Sheet

Automatically stores

- Customer Name
- Taxi Name
- Quantity
- Booking Status
- Timestamp

---

## 🤖 Bot Capabilities

The bot can:

- Welcome users
- Book Taxi
- Ask for missing booking information
- Check taxi availability
- Answer FAQs
- Save booking automatically
- Confirm booking status

---

### Welcome Menu

```
👋 Welcome to Sam Taxi Service!

I can help you with:

🚖 Book a Taxi
📋 Check Booking Status
❓ FAQs
🚘 Taxi Availability
```

---

### Booking Example

User

```
Book WagonR 2
```

Bot

```
Your booking for 2 WagonR taxis has been placed.

Status:
New
```

---

## 📂 Workflow Components

- Telegram Trigger
- AI Agent
- Groq Chat Model
- Taxi Details (Google Sheets)
- FAQ (Google Sheets)
- Orders (Google Sheets)
- Telegram Send Message

---
