
# 🛍️ SukiBot

SukiBot is a button-based Discord bot that helps you sell items directly inside your server. It features a clean shop interface, manual payment proof verification, mod-only controls, and dynamic inventory management — all without needing a website or external dashboard.

---

## ✨ Features

### 🛒 For Buyers
- View available items in a carousel format
- Place orders via button and modal
- Submit payment proof (image upload)
- Get notified when an order is approved or rejected
- View your order history

### 🛠️ For Moderators
- Add, update, delete, enable/disable items
- View incoming orders in a private mod channel
- Approve or reject submitted payment proofs
- Toggle shop open/closed
- Manually assign or rotate order reviewers (optional)

### 🕒 Shop Control
- Manual toggle (open/close)
- Optional daily schedule for auto-closing the shop
- Commands and buttons are automatically disabled when shop is closed

---

## 🧩 Tech Stack

- **Discord.js v14+**
- **Node.js**
- JSON or database (SQLite/MongoDB) for data storage (configurable)
- Slash commands (for setup, optional), but primarily button-based interaction

---

## 🗂 Project Structure

---
````
sukibot/
├── commands/
│   └── mod/
│       └── manageItems.js
├── components/
│   └── buttons/
│       ├── buyButton.js
│       └── approveReject.js
├── data/
│   ├── catalog.json
│   └── orders.json
├── events/
│   └── interactionCreate.js
├── utils/
│   └── itemManager.js
├── index.js
└── config.json

````
## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourname/sukibot.git
cd sukibot
````

### 2. Install dependencies

```bash
npm install
```

### 3. Set up environment

* Create a `config.json` or `.env` file:

```json
{
  "token": "YOUR_DISCORD_BOT_TOKEN",
  "clientId": "YOUR_CLIENT_ID",
  "guildId": "YOUR_TEST_GUILD_ID",
  "modChannelId": "MOD_APPROVAL_CHANNEL_ID"
}
```

### 4. Start the bot

```bash
node index.js
```

---

## 📦 Item Structure Example (`catalog.json`)

```json
[
  {
    "id": "shirt001",
    "name": "Black T-Shirt",
    "description": "Premium cotton fabric",
    "price": 299,
    "stock": 12,
    "active": true,
    "imageUrl": "https://link.to/image"
  }
]
```

---

## 📝 To-Do / Roadmap

* [x] Button-based item browsing
* [x] Modal-based ordering
* [x] Proof of payment system
* [x] Mod-only approval flow
* [x] Shop open/close control
* [ ] Loyalty system or discount codes
* [ ] Multiple currency/payment types
* [ ] Web dashboard (optional future)

---

## 📄 License

This project is licensed under the MIT License.
Feel free to fork and adapt it for your own shop needs.

---

## 🙏 Acknowledgments

Built with ❤️ for small online sellers, Discord communities, and shopkeepers who want a seamless and interactive selling experience inside Discord.

```

