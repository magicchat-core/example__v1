# 🪄 MagicChat Example — V1 (Instant Auth + Chat)

A **ready-to-use HTML + JS + CSS** example demonstrating **Instant Authentication + Chat** integration using [MagicChat.io](https://magicchat.io).  
Ideal for products **without a built-in authentication system**, offering an **out-of-the-box Auth + Chat** experience — so you can focus on your product logic while MagicChat handles the rest.

**License:** MIT

---

## 🚀 Overview

This repository showcases **MagicChat V1 (Instant Auth + Chat)** — designed for products and websites that need both authentication and real-time chat integrated seamlessly.  
It’s perfect for:

- 🧩 Projects without an existing login system  
- 💬 Products that want to provide instant chat and user authentication out-of-the-box  
- ⚙️ Developers who want to test MagicChat quickly and later migrate to a custom or existing auth setup  

MagicChat handles user onboarding, authentication, and chat — all within a few lines of code.  
Later, you can **export your users** and **migrate** to any authentication provider of your choice.

---

## 🧠 What is Instant Auth + Chat (V1)?

**V1** combines **authentication + chat** into one simple integration flow:  

- Auto-generated authentication layer (login/signup UI included)  
- Instant chat setup with admin & users  
- Customizable header (optional)  
- Seamless migration support when you’re ready for your own auth system  

---

## 🗂️ Folder Structure

```
example__v1/
├── index.html          # Main implementation page
├── style.css           # Basic styling
├── script.js           # Core logic for setup & initialization
└── package.json        # Local server configuration
```

---

## 💻 Getting Started

### 1. Clone this repository

```bash
git clone https://github.com/magicchat-io/example__v1.git
cd example__v1
```

### 2. Install dependencies

```bash
npm install
```

### 3. Start the local server

```bash
npm start
```

Now visit [http://localhost:8080](http://localhost:8080) — your V1 example should be running!

---

## ⚙️ Prerequisites

1. Sign up or log in to your [MagicChat.io](https://magicchat.io) account.  
2. Create a **new app** and select **Version: Instant Auth + Chat (V1)** during setup.  
3. Go to your app’s **detail page** and copy your credentials:  
   - **App Name**  
   - **API Key**  

---

## 🧩 Integration Steps

### 1. Load Required Scripts

Add the following inside your `<head>` tag (above all other scripts):

```html
<script src="https://cdn.socket.io/4.1.2/socket.io.min.js"></script>
<script src="https://magicchat-core.github.io/prod-ssc-client-cdns/bundle.js"></script>
```

---

### 2. Authentication UI Placement Options

MagicChat offers **two modes** for authentication UI:

#### 🧭 Full Header Mode
Automatically includes a functional header with:
- Login/logout controls  
- Profile management  
- Notifications  
- Branding & navigation

**Enable it** by setting the third parameter in `setUp` to `true`.

#### 🧩 Header-Less Mode
Choose this if your app already has its own header or UI layout.

---

### 3. Chat Placement in Your App

For most simple static sites, place the following code inside your `<script>` tag at the bottom of `index.html`:

```html
<script>
  document.addEventListener("DOMContentLoaded", async function () {
    // Step 1: Initial setup
    await window.magicchat_io.setUp(
      "<MAGICCHAT_APP_NAME>",
      "<MAGICCHAT_API_KEY>", 
      false // Flip to true for Full Header Mode
    );

    // Step 2: Initialize chat
    await window.magicchat_io.initialize({"app_version": "V1"});
  });
</script>
```

> ⚠️ The `setUp` function **must run before** `initialize`.

---

## 🧾 Parameter Reference

| Parameter | Type | Description |
|------------|------|-------------|
| `app_name` | string | Your MagicChat application name |
| `api_key` | string | Base64 encoded API key |
| `header_req` | boolean | Show header with auth controls (true = enabled) |

---

## 🧩 Example Use Case

- Simple informational website needing authentication + chat  
- SaaS MVPs needing instant onboarding & real-time user engagement  
- Admin + User chat system for early-stage products  

Once onboarded, users will automatically appear in your [MagicChat Admin Panel](https://admin.magicchat.io/) under their associated app.

---

## 📚 Learn More

- 🏠 [MagicChat.io](https://magicchat.io/) — Platform overview  
- 🧠 [Developers Docs](https://magicchat.io/developers) — Integration guides  
- ⚙️ [Admin Console](https://admin.magicchat.io/) — Manage users, apps & conversations  

---

## 🎉 Result

After integration:
- Users can sign up instantly and start chatting.  
- Admins can view and manage users in the [MagicChat Admin Panel](https://admin.magicchat.io/).  
- You can later export users and migrate to your own auth system with minimal effort.

---

## 🛠️ License

MIT © [MagicChat.io](https://magicchat.io)
