Mini Fiverr – Freelance Bidding Platform (MERN Stack)

A full-stack Freelance Bidding Platform inspired by Fiverr — built using the MERN stack (MongoDB, Express, React, Node.js).  
This project demonstrates authentication, project listings, bidding, and order management with a modern React (Vite) frontend and Node.js backend.

Features

- JWT Authentication (Login / Register for Buyers & Sellers)
- User Roles – Seller & Buyer dashboards
- Post Gigs / Projects and manage offers
- Place Bids and handle Orders
- Image Uploads for gigs and profiles
- MongoDB Models with Mongoose
- Modern React UI built with Vite + SCSS
- REST API structure with controllers, routes, middleware
- Ready for deployment (Render / Vercel / Netlify)

Project Structure

freelance-bidding-platform/
├── api/                     # Backend (Node + Express)
│   ├── controllers/         # Business logic
│   ├── middleware/          # Auth, error handling
│   ├── models/              # Mongoose schemas
│   ├── routes/              # API endpoints
│   ├── utils/               # Helper functions
│   ├── server.js            # Server entry point
│   ├── package.json
│   └── .env
├── client/                  # Frontend (React + Vite)
│   ├── public/
│   ├── src/
│   │   ├── components/      # Reusable UI components
│   │   ├── pages/           # Application pages
│   │   ├── App.jsx
│   │   ├── main.jsx
│   │   ├── data.js
│   │   └── app.scss
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
├── .gitignore
├── package.json             # Root package.json
├── yarn.lock / package-lock.json
└── README.md

Setup & Installation
Clone the Repository
```bash
git clone https://github.com/your-username/freelance-bidding-platform.git
cd freelance-bidding-platform

Backend Setup

```bash
cd api
npm install

Create a `.env` file inside `/api` with the following keys:
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/fiverr
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173

Start the server:
bash
npm run dev

The backend server will run at `http://localhost:5000`.

Frontend Setup
bash
cd client
npm install
npm run dev

Visit `http://localhost:5173` in your browser to access the app.

Scripts

Server (Backend):

json
"scripts": {
  "start": "node server.js",
  "dev": "nodemon server.js"
}

Client (Frontend):
json
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "preview": "vite preview"
}
Build & Deployment

1. Build frontend:
bash
cd client
npm run build

2. Serve static files from Express:
javascript
app.use(express.static('client/dist'));

3. Deploy backend + built frontend on Render, Railway, or Fly.io
   MongoDB Atlas for database
   Vercel / Netlify for standalone frontend

Tech Stack

| Layer           | Technology           |
| --------------- | -------------------- |
| Frontend        | React (Vite), SCSS   |
| Backend         | Node.js, Express     |
| Database        | MongoDB (Mongoose)   |
| Auth            | JWT (JSON Web Token) |
| Package Manager | npm / yarn           |

Future Enhancements

* Real-time chat using Socket.io
* Stripe or Razorpay payment integration
* Review & Rating system
* Responsive design improvements
* Notifications and email triggers

Credits

Inspired by Safak’s Fullstack Fiverr project.
Built purely for learning and portfolio purposes.

License

This project is licensed under the MIT License.

