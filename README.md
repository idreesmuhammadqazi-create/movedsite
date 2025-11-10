# 📦 Site Has Moved: Simple Redirect Landing Page

This repository contains a **minimal, single-file landing page** (`index.html`) designed to inform users and search engines that your website has permanently moved to a new domain or URL structure.

It is an ideal solution for quick site migrations where maintaining user experience and **SEO value** is critical.

---

## ✨ Key Features

* **Single File Deployment:** The entire solution is contained within a single `index.html` file (using inline CSS and JavaScript) for ultra-easy deployment.
* **Automatic Redirection:** Uses both a client-side **JavaScript countdown** and a robust **HTML `<meta refresh>` tag** to ensure users are redirected after a short, configurable delay (5 seconds by default).
* **Clear User Notification:** Provides a visible message and a **direct, clickable link** in case the automatic redirect is blocked or JavaScript is disabled.
* **SEO Fallback:** The design emphasizes the need for a server-side **HTTP 301 (Permanent Redirect)** status code, with the meta tag serving as the client-side signal.

---

## ⚙️ Configuration (How to Use)

To deploy this page, you only need to update the **target URL** inside the `index.html` file.

The target URL is hardcoded in **two** places for redundancy:

### 1. Update the HTML Meta Tag (SEO/Fallback)

Locate the `<meta>` tag in the `<head>` section and replace the example URL:

```html
<meta http-equiv="refresh" content="5;url=[https://pseudorun.vercel.app/](https://pseudorun.vercel.app/)">
// Target URL is set here and in the meta tag above
const NEW_URL = '[https://pseudorun.vercel.app/](https://pseudorun.vercel.app/)'; 
// ...
// In the <body>:
<a href="[https://pseudorun.vercel.app/](https://pseudorun.vercel.app/)">[https://pseudorun.vercel.app/](https://pseudorun.vercel.app/)</a>
