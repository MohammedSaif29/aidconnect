# 🤝 AidConnect

A donation platform that connects people who need help with donors who want to give. Beneficiaries post aid requests, an admin reviews and approves them, and donors browse requests and donate.

![Node.js](https://img.shields.io/badge/Node.js-Express-339933?logo=nodedotjs&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-better--sqlite3-003B57?logo=sqlite&logoColor=white)
![JWT](https://img.shields.io/badge/Auth-JWT_%2B_bcrypt-000000?logo=jsonwebtokens)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

---

## ✨ Features

- **Aid requests** — anyone can submit a request for help, which starts as *pending*
- **Admin verification** — admins review pending requests and mark them approved or rejected
- **Donations** — donors browse requests and donate; every donation is recorded against its request
- **Role-based login** — separate Donor and Admin flows with **JWT** authentication and **bcrypt**-hashed passwords
- **Admin dashboard** — view pending requests and the full donation history
- **Persistent storage** — SQLite database with users, requests and donations tables and foreign-key constraints

## 🛠️ Tech Stack

Node.js · Express · better-sqlite3 · JSON Web Tokens · bcryptjs · HTML · CSS · JavaScript

## 🔌 API

| Method | Endpoint | Access | Description |
|---|---|---|---|
| `POST` | `/api/auth/login` | Public | Log in as donor or admin |
| `GET` | `/api/requests` | Public | List aid requests with their status |
| `GET` | `/api/requests/:id` | Public | Request details |
| `POST` | `/api/requests` | Public | Submit a new aid request |
| `POST` | `/api/donate` | Public | Record a donation to a request |
| `GET` | `/api/admin/requests/pending` | Admin | Requests awaiting review |
| `PATCH` | `/api/requests/:id` | Admin | Approve or reject a request |
| `GET` | `/api/admin/donations` | Admin | All donations |

## 🚀 Run Locally

```bash
npm install
npm install better-sqlite3
node scripts/set-admin-password.js "choose-a-strong-password"   # set the admin password
npm start                                                       # http://localhost:3000
```

Set `JWT_SECRET` as an environment variable before running in any shared environment.

## 👤 Author

**Mohammed Saif** — B.Tech CSE
[LinkedIn](https://www.linkedin.com/in/saif-mohammed-939902335/) · [GitHub](https://github.com/MohammedSaif29)
