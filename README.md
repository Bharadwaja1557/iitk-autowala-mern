# IITK AutoWala 🛺

### <a href="https://iitk-autowala.netlify.app"> 👉  Live link </a>


A lightweight full-stack web application that enables riders to discover nearby available drivers in real time. The system supports three roles — **Rider**, **Driver**, and **Admin** — and was built as part of a hackathon with a focus on simplicity, reliability, and fast deployment.

---

## 🚀 Features

### Rider
- Select a zone and view available drivers in that zone and nearby zones  
- Drivers are grouped by zone  
- Click-to-call support using phone links  
- Auto-refresh to keep driver list updated  

### Driver
- Register using name, phone number, vehicle type, and zone  
- Toggle availability (**Available / Busy**)  
- Change zone and re-announce availability  
- Visibility expires automatically after a fixed duration if not refreshed  
- Countdown indicator showing remaining visibility time  

### Admin
- Hidden admin access (tap-based entry)  
- View all registered drivers with full metadata  
- See driver status: **Active / Expired / Offline**  
- Force drivers offline when required  
- Auto-refresh and manual refresh support  

---

## 🧠 Core Logic
- Zone-based discovery with predefined nearby-zone mapping  
- Time-based visibility: drivers are shown to riders only if they have recently declared availability  
- Stateless REST APIs with clear separation of concerns  
- Single-page frontend with role-based panels  

---

## 🛠️ Tech Stack

### Frontend
- React (Hooks)  
- Deployed on Netlify  

### Backend
- Node.js  
- Express.js  
- RESTful API design  
- Deployed on Render  

### Database
- SQL (hosted)  
- Stores drivers, zones, availability status, and timestamps  

---

## 📁 Project Structure (High Level)

```
driver-discovery/
├── backend/
│   ├── index.js
│   ├── db.js
│   ├── models/
│   │   └── Driver.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── App.js
│   │   └── panels/
│   │       ├── RiderPanel.js
│   │       ├──DriverPanel.js
│   │       └── AdminPanel.js
│   └── package.json
│
└── README.md
```

---

## 🌍 Deployment
### <a href="https://iitk-autowala.netlify.app"> 👉 Live link </a>
- **Frontend:** Netlify  
- **Backend:** Render  
- **Database:** FreeSQLdatabase  

Environment variables are used for API URLs and database credentials.

---

## 📌 Notes
- The system is designed to work with minimal driver interaction  
- Emphasis was placed on real-world constraints, such as unreliable connectivity and simple UIs  
- The project prioritizes correctness, clarity, and deployability over heavy abstractions  
