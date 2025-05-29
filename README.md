# Real-Time-Location-Tracker-For-MultiVendor-Delivery-Platform
This project is a real-time location tracking system designed for a multivendor delivery marketplace, inspired by popular services like Rapido and Dunzo. It provides an interactive platform where vendors, delivery partners, and customers can manage and track deliveries live and efficiently. 
Vendors have access to a dashboard where they can view their orders and assign delivery partners to fulfill those orders. This enables vendors to maintain control over their shipments and monitor delivery progress.

Delivery partners use a dedicated dashboard to start deliveries and send continuous live location updates. Location data is transmitted either through the device’s geolocation API or simulated coordinates, providing flexibility during testing.

Customers can track the delivery partner’s live location on an interactive map, which updates automatically every few seconds. This transparency enhances customer experience by allowing them to monitor the real-time progress of their orders.

The backend, built with Node.js, Express, and TypeScript, implements secure JWT authentication for vendors, delivery partners, and customers. It uses MongoDB for data persistence and Socket.IO for real-time communication between clients and the server. The system ensures data privacy by restricting vendors to only view their own orders.

The frontend is developed with Next.js and TypeScript, utilizing Leaflet.js and OpenStreetMap to render the customer tracking map. This combination ensures a responsive, scalable, and user-friendly interface.

Overall, this project showcases modern full-stack development techniques, emphasizing real-time data handling, role-based access control, and interactive mapping. It is a practical demonstration of building a scalable and secure delivery tracking platform.
Tech Stack

    Frontend: Next.js, TypeScript, Leaflet.js, OpenStreetMap

    Backend: Node.js, Express, TypeScript, Socket.IO

    Database: MongoDB

    Authentication: JWT (JSON Web Tokens)

    Real-time Communication: Socket.IO (WebSockets)

Features
Vendor

    Register/Login

    View list of orders

    Assign delivery partners to orders

Delivery Partner

    Register/Login

    View assigned orders

    Start delivery and share live location (real or simulated)

Customer

    Track assigned delivery partner’s live location on a map

    Auto-updating map every 2–3 seconds

Setup Instructions
Prerequisites

    Node.js (v14 or higher)

    MongoDB instance (local or cloud)

    npm or yarn

Backend Setup

cd backend
npm install
cp .env.example .env
# Update .env with your MongoDB URI and JWT_SECRET
npm run dev

Frontend Setup

cd frontend
npm install
npm run dev

Usage

    Open the frontend app at http://localhost:3000

    Register as a vendor or delivery partner

    Vendors can create orders and assign delivery partners

    Delivery partners can start delivery and share location

    Customers can track the live location of their delivery partner on the tracking page (/track/[orderId])

Project Structure

/backend
  ├── src
  │    ├── controllers
  │    ├── models
  │    ├── routes
  │    ├── middlewares
  │    └── index.ts
  ├── package.json
  └── .env.example

/frontend
  ├── pages
  ├── components
  ├── styles
  ├── public
  ├── package.json
  └── next.config.js



