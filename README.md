# 🐾 FetchBot — Pet Products Conversational AI

FetchBot is a **smart virtual assistant** built with **Dialogflow CX**, **Google Apps Script**, and **Google Sheets** to help pet owners order food, toys, and grooming products — or check order status — instantly via chat.

---

## 📌 **Features**
- Order pet food, toys, accessories, grooming products.
- Check real-time order status.
- Logs orders to **Google Sheets** using **Apps Script Webhooks**.
- Extensible for Twilio/WhatsApp & CCAI Telephony (voice).

---

## ⚙️ **Tech Stack**
- **Dialogflow CX** — Intents, Entities, Flows, Pages
- **Google Apps Script** — Webhook for logging & fetching orders
- **Google Sheets** — Order database
- **(Optional)** Twilio & WhatsApp channel
- **(Planned)** CCAI Telephony for voice calls

---

## ✅ **How it works**
1. User talks to FetchBot → selects product → provides quantity & name.
2. FetchBot logs order details to Google Sheets (via webhook).
3. User can check status by providing Order ID → status fetched from Sheet.

---

## 🗂️ **Project Structure**
📁 FetchBot/
├─ 📄 README.md
├─ 📄 OrderWebhook.gs (Google Apps Script for logging orders)
├─ 📄 FetchStatusWebhook.gs (Google Apps Script for fetching order status)
├─ 📄 flowchart.png
├─ 📄 slides.pdf
├─ 📄 screenshots/ (conversation & dashboard images)


---

## 🚀 **Setup & Deployment**
1️⃣ **Deploy Google Apps Script**  
- `OrderWebhook.gs` → Deploy as Web App → Get POST URL → Add to Dialogflow Order Confirmation Page fulfillment.  
- `FetchStatusWebhook.gs` → Deploy as Web App → Get GET URL → Add to Dialogflow Fetch Status Page fulfillment.

2️⃣ **Connect Parameter Presets**  
- Ensure `customerName`, `productCategory`, `productName`, `quantity` in Dialogflow **intent routes** match Apps Script keys.

3️⃣ **Test End-to-End**
- Place an order → Confirm Google Sheets logs.
- Check status → Fetch order by ID.

---

## 📷 **Screenshots**
- Conversation example (ordering)
- Conversation example (fetch status)
- Google Sheet with logged orders
- Flowchart diagram of FetchBot

---

## 🗂️ **Resources**
- [Dialogflow CX Docs](https://cloud.google.com/dialogflow/cx/docs)
- [Google Apps Script Docs](https://developers.google.com/apps-script)
- [Twilio WhatsApp](https://www.twilio.com/whatsapp)

---

## 🤝 **Contributing**
Feel free to fork, improve or adapt for your own conversational AI demos!

---

## 📬 **Contact**
Made by **Thessalony Dudde**  
💼 LinkedIn : https://www.linkedin.com/in/thessalony-dudde-533636243/
📧 Your Email : thessalonydudde@gmail.com
