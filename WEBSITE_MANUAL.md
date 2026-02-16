# 📘 Website Maintenance Manual

This guide covers how to manage your **Digital Business Card** and **Shortlist Dachshunds** websites.

## 🌟 The "Golden Workflow"
We are using the professional standard: **GitHub + Cloudflare Pages**.
- **GitHub:** Stores your code safely in the cloud (like Dropbox for code).
- **Cloudflare Pages:** Takes that code and turns it into a fast, secure website.

---

## 🚀 Part 1: Initial Setup (One-Time Only)

### 1. Create the Repository (GitHub)
1.  Log in to [GitHub.com](https://github.com).
2.  Click the **+** (top right) -> **New repository**.
3.  **Name:** `digital-business-card` (or `shortlist-dachshunds`).
4.  **Public/Private:** Public is fine (and free).
5.  Click **Create repository**.
6.  Click the link that says **"uploading an existing file"**.
7.  Drag in your files (`index.html`, `style.css`, `profile.jpg`).
8.  Commit changes.

### 2. Connect to the World (Cloudflare Pages)
*⚠️ Key Step: Watch out for "Workers" vs "Pages"*

1.  Log in to [Cloudflare Dashboard](https://dash.cloudflare.com).
2.  **Find the Menu:** In the left sidebar, look under **Build** -> **Compute** -> **Workers & Pages**.
3.  Click **Create application**.
4.  **UI TRAP:** Look at the very bottom of the screen for a link that says: **"Looking to deploy Pages? Get started"**. Click that.
5.  Click **Connect to Git**.
6.  Select your GitHub account and the new repo.
7.  **Build Settings:** Leave "Framework preset" as `None` and "Build command" empty.
8.  Click **Save and Deploy**.
    *   *Result:* You get a live link like `digital-business-card.pages.dev`.

### 3. Add Your Custom Domain
### 3. Add Your Custom Domain (The "Missing Link")
*Crucial: connecting your domain to the Pages project.*

1.  In the Cloudflare Dashboard sidebar, go to **Workers & Pages**.
2.  Click on your project name (e.g., `gavin-lai`).
3.  Click the **Custom domains** tab (near the top).
4.  Click **Set up a custom domain**.
5.  Type your domain name (e.g., `gavinlai.com`).
6.  Click **Continue** -> **Activate Domain**.
    - Since you already set up Cloudflare DNS earlier, this should be instant.

### 4. Email Setup (Cloudflare Email Routing)
*How to get `hello@yourdomain.com` without paying for GSuite.*

1.  In Cloudflare Dashboard, select your domain.
2.  Go to **Email** -> **Routing** in the sidebar.
3.  Click **Create address**.
4.  **Custom address:** Enter the alias you want (e.g., `hello` or `contact`).
5.  **Destination:** Enter your personal email (e.g., Gmail).
6.  **Verify:** Check your personal inbox for a verification email from Cloudflare and click the link.
7.  **Enable:** Go back to Cloudflare and ensure the status is **Active**.

---

## 🔄 Part 2: How to Update Your Site
*Example: You want to change your job title or add a new link.*

1.  **Edit the file on your computer** (just like we did today).
2.  **Test it** by opening `index.html` in Chrome to make sure it looks right.
3.  **Go to your GitHub Repository**.
4.  Click **Add file** -> **Upload files**.
5.  Drag the updated `index.html` (or whatever you changed) into the box.
6.  Write a note (e.g., "Updated job title") and click **Commit changes**.

**✨ Magic:** Cloudflare sees the change on GitHub and **automatically updates your live website** within seconds!

---

## 🛠️ Project Cheat Sheet

### 1. Digital Business Card
- **Folder:** `C:\Users\thega\.gemini\antigravity\scratch\digital_business_card`
- **Key Files:** `index.html` (Content), `style.css` (Design).

### 2. The Shortlist Dachshunds
- **Folder:** `C:\Users\thega\.gemini\antigravity\scratch\shortlist_dachshunds`
- **Key Files:** `index.html`, `style.css`, `puppy.jpg`.
