# ⬡ QUANTUM BASTION

A secure, animated web proxy with user accounts and admin monitoring.

---

## 🚀 GitHub Pages Setup

1. Upload all 4 files to a new GitHub repository
2. Go to **Settings → Pages → Deploy from branch → main → / (root)**
3. Your site will be live at `https://yourusername.github.io/repo-name`

---

## 🔑 Admin Login

Find the `ADMIN_KEY` variable in `index.html` and change it to your desired password:

```js
const ADMIN_KEY = 'QB_ADMIN_2024_SECURE_#$%';
```

This key is entered in the **Admin Access** section on the login page.

---

## ⚡ Features

- **Animated Login Page** — Particle effects, hex grid, glitch animations
- **User Accounts** — Register/login, data saved per-browser via localStorage
- **DuckDuckGo Search** — Powered by DuckDuckGo
- **URL Proxy** — Browse URLs through corsproxy.io
- **Admin Dashboard** — User management, search stats, activity logs
- **Screen Viewer** — WebRTC-based screen viewing (requires user's browser permission)

---

## 🖥 Screen Viewer

Uses **PeerJS WebRTC** peer-to-peer connections:

1. User visits the proxy page → their Peer ID is auto-generated and saved
2. Admin goes to **Admin → Screen View**
3. Admin enters the user's Peer ID and clicks **REQUEST VIEW**
4. User's browser shows a screen share permission prompt
5. If accepted, live screen feed appears in the admin panel

> The user's browser will always show a native OS-level permission dialog for screen sharing. You can find user Peer IDs in the **Users** panel of the admin dashboard.

---

## 📁 Files

| File | Purpose |
|------|---------|
| `index.html` | Login / Register page |
| `proxy.html` | Main proxy & search interface |
| `admin.html` | Admin control panel |
| `README.md` | This file |

---

## ⚠️ Notes

- User data is stored in **localStorage** — it's per-device/per-browser
- The proxy uses **corsproxy.io** (free, rate-limited) — for production use your own CORS proxy
- Screen viewing uses **PeerJS free cloud** signaling — host your own PeerJS server for production
- All screen sharing requires explicit browser permission from the user
