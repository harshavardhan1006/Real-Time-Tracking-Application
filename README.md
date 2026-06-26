# Real-Time Tracking Application

A real-time location tracking web application built using **Node.js**, **Express.js**, **Socket.IO**, and **Leaflet.js**. The application enables multiple users to share and view live geographic locations on an interactive map in real time.

---

## Features

* Real-time location tracking using browser geolocation
* Live location updates using WebSockets
* Interactive map visualization with Leaflet
* Multiple users visible simultaneously on the map
* Automatic marker removal when a user disconnects
* Responsive full-screen map interface

---

## Tech Stack

### Frontend

* HTML
* CSS
* JavaScript
* Leaflet.js

### Backend

* Node.js
* Express.js
* Socket.IO

---

## How It Works

1. When a user opens the application, the browser requests location permission.
2. After permission is granted, the Geolocation API continuously tracks the user's position.
3. The frontend sends latitude and longitude to the server using Socket.IO.
4. The backend receives the coordinates and broadcasts them to all connected clients.
5. Each client receives the updated coordinates and updates markers on the Leaflet map.
6. If a user disconnects, their marker is automatically removed from the map.

---

## Socket Events

### Client → Server

* **send-location**
  Sends the user's current latitude and longitude to the server.

### Server → Client

* **receive-location**
  Broadcasts location updates of connected users to all clients.

* **user-disconnected**
  Removes the disconnected user's marker from the map.
