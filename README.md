# 🚗 GoFAST – Carpooling App for FAST NUCES Students

A web-based carpooling platform connecting FAST NUCES students for safer, affordable, and eco-friendly commutes.

[![React](https://img.shields.io/badge/React-18+-61DAFB.svg?logo=react)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-339933.svg?logo=node.js)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-6+-47A248.svg?logo=mongodb)](https://www.mongodb.com/)
[![Express](https://img.shields.io/badge/Express-4+-000000.svg?logo=express)](https://expressjs.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3+-38B2AC.svg?logo=tailwind-css)](https://tailwindcss.com/)

---

## 📖 Project Overview

GoFAST is a web application designed to connect FAST NUCES students for carpooling, helping to:

- Reduce transportation costs
- Promote eco-friendly travel
- Build a stronger student community
- Ensure safety** through verified university email access

Access is restricted to verified `@nu.edu.pk` email addresses to ensure trust and security within the student community.

---

## Introduction and Background

While popular ride-sharing apps like InDrive and Yango exist, they don't address the specific needs of university students. **GoFAST** fills this gap by offering a campus-specific, feature-rich carpooling experience that:

- Reduces traffic congestion around campus
- Minimizes carbon footprint through shared rides
- Creates a trusted network of student riders
- Offers cost-effective transportation solutions

---

## ❗ Problem Statement

FAST NUCES students face several commuting challenges:

-  High individual transportation costs
-  No centralized platform for student ride-sharing
-  Safety concerns with external ride-sharing services
-  Inefficient coordination among students traveling similar routes
-  Lack of trust in existing platforms

GoFAST solves these issues by providing a trusted, university-exclusive platform where students can safely coordinate carpools within their own community.

---

## ✨ Core Features

### 🔐 1. User Authentication (Login/Signup)

- Verified Registration: Sign up using valid FAST university email (`@nu.edu.pk`)
- Secure Login: JWT (JSON Web Token) authentication
- Complete Profile:
  - Full Name
  - Department
  - Batch/Year
  - Contact Information
  - Profile Picture (optional)

### 🚙 2. Carpool Post System

Create detailed ride posts including:

- Pickup location
- Drop-off location
- Departure time
- Number of available seats
- Ride preferences (e.g., female-only, department-specific)
- Cost sharing details (optional)

Posts are automatically visible to relevant students based on their preferences and routes.

### 🔍 3. Search & Filter System

Advanced filtering options:

- By Route: Specific pickup/drop-off locations
- By Time: Departure time windows
- By Preferences: Gender-specific rides
- By Community: Department and batch filters
- By Rating: Minimum driver/rider ratings
- Map View (Optional): Visual route selection interface

### 📲 4. Booking & Requests

Seamless booking workflow:

- Send ride requests to post creators
- Accept or Decline incoming requests
- Real-time confirmation notifications
- Email alerts for both parties

### ⭐ 5. Ride Reviews & Ratings

Build trust through feedback:

- Rate rides on a 1-5 star scale
- Leave detailed text reviews
- View user rating history
- Filter search results by minimum rating
- Report inappropriate behavior

---

## 🛠️ Tech Stack (MERN)

### Frontend
- **React.js** - UI framework
- **React Router** - Client-side routing
- **Tailwind CSS** - Utility-first styling
- **Socket.io Client** - Real-time communication
- **Axios** - HTTP requests

### Backend
- Node.js - Runtime environment
- Express.js - Web framework
- JWT - Authentication & authorization
- Socket.io - WebSocket server for real-time features
- Bcrypt - Password hashing

### Database
- MongoDB - NoSQL database
- Mongoose - ODM (Object Data Modeling)

### Additional Tools
- Nodemailer - Email verification
- Multer - File upload handling
- Google Maps API - Location services (optional)

---

## 🎯 Additional Features

### 💬 1. Direct Messaging System

- Real-time chat using WebSockets
- Push notifications for new messages
- Chat history storage
- File sharing capabilities (images, documents)
- Read receipts

### 🗺️ 2. Saved Routes & Ride History

- Save frequently used routes
- Quick post creation from saved routes
- Complete ride history with details
- Past feedback and ratings
- Export ride data

### 📍 3. Live Location Sharing

- Optional real-time GPS tracking during rides
- Enhanced safety for riders
- ETA (Estimated Time of Arrival) updates
- Emergency contact notifications
- Privacy controls

### 🌙 4. Dark Mode & UI Customization

- System-based theme detection
- Manual dark/light mode toggle
- Custom accent colors
- Accessibility features
- Responsive design for all devices

---

## 📋 Project Architecture

```
GoFAST/
├── client/                 # Frontend React application
│   ├── public/
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Route-based pages
│   │   ├── context/       # React Context API
│   │   ├── hooks/         # Custom React hooks
│   │   ├── services/      # API service calls
│   │   ├── utils/         # Helper functions
│   │   └── App.js
│   └── package.json
│
├── server/                # Backend Node.js application
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── models/           # MongoDB schemas
│   ├── routes/           # API routes
│   ├── middleware/       # Custom middleware
│   ├── utils/            # Helper functions
│   └── server.js
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (v6 or higher)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/GoFast-CarpoolApp.git
   cd GoFast-CarpoolApp
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   # Server Configuration
   PORT=5000
   NODE_ENV=development

   # Database
   MONGO_URI=your_mongodb_connection_string

   # JWT Secret
   JWT_SECRET=your_jwt_secret_key
   JWT_EXPIRE=7d

   # Email Configuration
   EMAIL_SERVICE=gmail
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASSWORD=your_app_password

   # Optional: Google Maps API
   GOOGLE_MAPS_API_KEY=your_api_key
   ```

4. **Run the application**
   ```bash
   npm run start
   ```

   The app will be available at:
   - Frontend: `http://localhost:3000`
   - Backend: `http://localhost:5000`

### Development Mode

Run frontend and backend concurrently:
```bash
npm run dev
```

---

## ✅ Completeness Criteria

The project is considered complete when the following are functional:

- ✅ Verified sign-up with `@nu.edu.pk` email
- ✅ Complete user profile creation and management
- ✅ Carpool post creation with all details
- ✅ Advanced search and filtering system
- ✅ Booking system with request management
- ✅ Real-time messaging between users
- ✅ Review and rating system
- ✅ Live location sharing (optional)
- ✅ Ride history and saved routes
- ✅ Dark mode and UI customization
- ✅ Application deployed and accessible to students

---

## 📱 Usage Guide

### For Riders

1. **Sign up** with your FAST email
2. **Complete your profile** with accurate information
3. **Search for rides** using filters
4. **Send a request** to join a carpool
5. **Communicate** with the driver via chat
6. **Rate and review** after the ride

### For Drivers

1. **Create a ride post** with all details
2. **Review incoming requests** from riders
3. **Accept riders** that match your preferences
4. **Coordinate** pickup details via chat
5. **Share live location** (optional) during the ride
6. **Collect ratings** and build your reputation

---

## 🔒 Security Features

- **Email Verification**: Only `@nu.edu.pk` emails allowed
- **JWT Authentication**: Secure token-based auth
- **Password Encryption**: Bcrypt hashing
- **Rate Limiting**: Prevent API abuse
- **Input Validation**: Sanitize all user inputs
- **HTTPS**: Encrypted data transmission
- **Privacy Controls**: User data protection

---

## 🌍 Environmental Impact

By facilitating carpooling, GoFAST contributes to:

- 🌱 Reduced carbon emissions
- 🚗 Less traffic congestion
- ⛽ Lower fuel consumption
- 🌏 Sustainable campus community

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👥 Authors

**FAST NUCES Development Team**

- GitHub: [@ezza-abdullah1](https://github.com/ezza-abdullah1)

---

## 📞 Support

For support, email: support@gofast.nu.edu.pk

---

## 🎯 Future Enhancements

- 🔔 Push notifications for mobile devices
- 💳 In-app payment integration
- 🏆 Gamification and rewards system
- 📊 Analytics dashboard for administrators
- 🌐 Multi-campus support
- 🤖 AI-based route optimization
- 📱 Native mobile applications (iOS/Android)

---

## 💡 Conclusion

**GoFAST** is designed to revolutionize the daily commute for FAST NUCES students by making ride-sharing easier, safer, and more reliable. With a focus on trust, convenience, and sustainability, it creates a connected and eco-conscious student community that benefits everyone.

**Join the movement towards smarter, greener commuting! 🚗💚**

---

## ⭐ Show Your Support

Give a ⭐️ if this project helps you commute better!

---

**Built with 💙 for the FAST NUCES community**
