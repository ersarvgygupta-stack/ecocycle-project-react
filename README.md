# ♻️ EcoCycle — E-Waste Collection & EPR Record Platform

> **Building a cleaner tomorrow** — A full-stack platform that connects citizens, authorized collection partners, recyclers, and participating organizations to collect e-waste responsibly and keep auditable recycling and EPR records.
---
> **🌐 **Live Demo:** [https://ecocycle-sage.vercel.app/](https://ecocycle-sage.vercel.app/)**
---
## 🧠 About the Project

**EcoCycle** is a full-stack web application built to make e-waste collection simple, trackable, and accountable.

The platform enables:

- Citizens to request pickup of old electronics
- Collection centers and recyclers to update pickup status and enter verified weight
- Admins to approve partners and maintain recycling records
- Participating organizations to have their EPR (Extended Producer Responsibility) records maintained
- Every important change to be saved in an audit log

The system provides separate views for **Citizens**, **Partners**, and **Admins**, so each person sees only what they need.

---

## ✨ Features

- 🔐 **Secure Registration & Login** — Passwords are hashed with bcrypt, never stored in plain text
- 👥 **Role-Based Access** — Citizen, Partner, and Admin dashboards, checked on the server
- 📝 **Pickup Requests** — Citizens request collection with device type, quantity, and address
- 🚚 **Status Tracking** — Requested → Scheduled → Picked Up → Delivered to Recycler → Verified
- ⚖️ **Verified Weight Entry** — Partners record the verified weight in kg
- ✅ **Partner Approval** — Admin approves or rejects collection centers and recyclers
- 🏢 **Organizations** — Admin maintains the list of participating organizations
- 📄 **EPR Records** — Admin links verified requests to organizations (Verified requests only)
- 🧾 **Audit Log** — Every status change, approval, and EPR record shows who did it and when
- 📈 **Admin Overview** — Simple counts for requests, partners, weight, and EPR records
- ⏳ **Loading, Empty & Error States** — Clear messages on every data page
- 📱 **Responsive Design** — Works on desktop and mobile with a dark and teal theme

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Frontend** | React JS , JSX, React Router, Axios, CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB Atlas, Mongoose |


---

## 👤 User Roles

| Role | What They Can Do |
|------|------------------|
| 🙋 **Citizen** | Register, log in, request pickups, track own requests |
| 🚚 **Partner** | Register as a center or recycler, get approved, update status, enter verified weight |
| 🛡️ **Admin** | Approve partners, view all requests, manage organizations, create EPR records, view audit log |

> Participating organizations do not log in. The admin creates and maintains their records.

---

## 🔄 How It Works

1. A citizen registers and logs in.
2. The citizen submits an e-waste pickup request.
3. A collection partner registers and waits for admin approval.
4. The admin approves the partner.
5. The approved partner schedules the pickup and marks it as picked up.
6. The device is delivered to a recycler.
7. The recycler enters the verified weight, and the request becomes **Verified**.
8. The admin creates an EPR record linking the verified request to an organization.
9. The audit log records every step with who did it and when.

---

## 🏠 Main Modules

| Module | Description |
|--------|-------------|
| 👤 **Authentication** | Registration and login with hashed passwords |
| 📦 **Requests** | Create, view, and update collection requests |
| 🚚 **Partner Dashboard** | Update status and enter verified weight |
| ✅ **Partner Approval** | Admin approves or rejects partners |
| 🏢 **Organizations** | Participating organization records |
| 📄 **EPR Records** | Recycling records linked to organizations |
| 🧾 **Audit Log** | Who changed what, and when |
| 📈 **Admin Overview** | Counts and totals from the database |


---

## 📁 Project Structure

```
int252-project/
├── public/
├── src/
│   ├── Components/        Navbar, Footer, StatusBadge, StatCard, ProtectedRoute
│   ├── Pages/             Home, Login, Register, MyRequests, NewRequest,
│   │   │                  RequestDetails, PartnerDashboard
│   │   └── Admin/         AdminLayout, AdminHome, AdminPartners, AdminRequests,
│   │                      AdminOrganizations, AdminEpr, AdminAudit
│   ├── EcoCycle.jsx       App routes
│   ├── EcoCycle.css       Project styles
│   ├── Axios.jsx          Axios setup
│   └── main.jsx           Entry point
├── server.js              Express server and API routes
├── models.js              Mongoose models
├── seedAdmin.js           Creates the admin account
├── .env.example           Environment variable template
├── vite.config.js
└── package.json
```
---


## 📊 Future Improvements

- 🔑 JWT or signed-session authentication
- 📧 Email and SMS notifications
- 🔍 Search and filters
- 📄 CSV/PDF report export
- 🗺️ Pickup location map
- 📱 Progressive Web App support

---

## 👨‍💻 Developed By

**Sarvgy Gupta**

- 📧 er.sarvgygupta@gmail.com
- 💻 Full Stack Developer
- 🎓 B.Tech Computer Science Engineering

---

## 🔗 Project Links

- 🌐 **Live Demo:** [https://ecocycle-sage.vercel.app/](https://ecocycle-sage.vercel.app/)
- 💻 **GitHub Repository:** https://github.com/ersarvgygupta-stack/ecocycle-project-react
