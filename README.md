# Telegram Print Order Bot

## 📌 Project Overview
This project is a Telegram bot designed to automate print service orders.  
Users can submit PDF files or page counts, select print format and number of copies, and upload payment confirmation — all through Telegram.

The bot automatically calculates pricing, tracks orders, and notifies the admin in real time.

## ⚙️ Features
- Collects customer full name and phone number
- Accepts PDF files and automatically counts pages
- Supports A4 and A5 print formats
- Calculates total price and advance payment
- Accepts payment screenshots
- Sends all order details to admin
- Saves orders to a local file
- Admin-only statistics command

## 📊 Business Logic
- A4 pricing: `(pages × 200 + 15000) × copies`
- A5 pricing: calculated proportionally
- Advance payment: 50% of total price
- Orders are logged with timestamp

## 🛠 Tools & Technologies
- Python
- python-telegram-bot
- PyMuPDF (PDF page counting)
- File-based data storage
- Telegram Bot API

## 🔍 How It Works
1. User starts the bot with `/start`
2. Bot collects:
   - Full name
   - Phone number
3. User uploads a PDF file or enters page count
4. User selects print format (A4 / A5)
5. User enters number of copies
6. Bot calculates price and advance payment
7. User uploads payment screenshot
8. Order is sent to admin and saved to file

## 👮 Admin Features
- Receives all orders instantly
- Receives uploaded PDFs and payment screenshots
- Can check statistics using `/stat`
- Order history stored in `orders.txt`

## ▶️ How to Run the Project

### 1. Install dependencies
```bash
pip install python-telegram-bot pymupdf
