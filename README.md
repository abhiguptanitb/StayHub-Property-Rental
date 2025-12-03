# 🏠 StayHub - Property Rental Platform

<div align="center">

![StayHub](https://img.shields.io/badge/StayHub-Property%20Rental-6366f1?style=for-the-badge&logo=airbnb&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-4.x-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white)

**A modern, full-stack property rental platform built with cutting-edge technologies**

[Features](#-features) • [Tech Stack](#-tech-stack) • [Installation](#-installation) • [Usage](#-usage) • [Project Structure](#-project-structure)

</div>

---

## 📖 About

StayHub is a comprehensive property rental platform that enables users to discover, list, and manage vacation rentals. Built with a focus on user experience and modern design, it provides a seamless interface for property owners and travelers to connect.

### ✨ Key Highlights

- 🎨 **Modern UI/UX** - Beautiful, responsive design with smooth interactions
- 🔐 **Secure Authentication** - Robust user authentication and authorization
- 📸 **Image Management** - Cloud-based image storage with Cloudinary
- 🗺️ **Interactive Maps** - Mapbox integration for property location visualization
- ⭐ **Review System** - Comprehensive rating and review functionality
- 📱 **Fully Responsive** - Works seamlessly on all devices

---

## 🚀 Features

### 🔑 Authentication & Authorization
- ✅ User registration and login
- ✅ Secure session management with Express-Session
- ✅ Passport.js for authentication
- ✅ Protected routes and authorization

### 🏡 Property Listings
- ✅ Create, read, update, and delete property listings
- ✅ Image upload with Cloudinary integration
- ✅ Property details with location, pricing, and descriptions
- ✅ Interactive map integration with Mapbox
- ✅ Owner-based access control

### ⭐ Reviews & Ratings
- ✅ Leave reviews on properties
- ✅ Star-based rating system
- ✅ Review management (edit/delete own reviews)
- ✅ Display all reviews with user information

### 🎨 User Interface
- ✅ Modern, clean design
- ✅ Responsive layout for all screen sizes
- ✅ Flash messages for user feedback
- ✅ Smooth animations and transitions
- ✅ Professional color scheme

---

## 🛠️ Tech Stack

### Backend
- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling

### Frontend
- **EJS** - Embedded JavaScript templating
- **Bootstrap 5** - CSS framework
- **Font Awesome** - Icon library
- **Custom CSS** - Modern styling with CSS variables

### Authentication & Security
- **Passport.js** - Authentication middleware
- **Express-Session** - Session management
- **Joi** - Data validation

### Third-Party Services
- **Cloudinary** - Cloud-based image storage
- **Mapbox** - Interactive maps and geocoding
- **Multer** - File upload handling

---

## 📦 Installation

### Prerequisites

- Node.js (v14 or higher)
- MongoDB Atlas account (or local MongoDB)
- Cloudinary account
- Mapbox account

### Step 1: Clone the Repository

```bash
git clone https://github.com/abhiguptanitb/StayHub-Property-Rental.git
cd StayHub
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Environment Variables

Create a `.env` file in the root directory:

```env
# MongoDB
ATLASDB_URL=your_mongodb_atlas_connection_string

# Cloudinary
CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret

# Session
SECRET=your_random_session_secret_key

# Mapbox
MAP_TOKEN=your_mapbox_access_token

# Environment
NODE_ENV=development
```

### Step 4: Run the Application

```bash
npm start
```

The server will start on `http://localhost:8080`

---

## 💻 Usage

### Getting Started

1. **Sign Up** - Create a new account
2. **Log In** - Access your account
3. **Explore** - Browse available properties
4. **List Property** - Add your own property listing
5. **Review** - Leave reviews on properties you've visited

### User Roles

- **Guest** - Browse and view listings
- **Authenticated User** - Create listings, leave reviews
- **Property Owner** - Manage own listings (edit/delete)

---

## 📁 Project Structure

```
StayHub/
│
├── 📂 controllers/          # Business logic
│   ├── listings.js         # Listing operations
│   ├── reviews.js          # Review operations
│   └── user.js             # User authentication
│
├── 📂 models/              # Database models
│   ├── listing.js          # Listing schema
│   ├── review.js           # Review schema
│   └── user.js             # User schema
│
├── 📂 routes/              # Route definitions
│   ├── listing.js          # Listing routes
│   ├── review.js           # Review routes
│   └── user.js             # User routes
│
├── 📂 views/               # EJS templates
│   ├── includes/           # Reusable components
│   │   ├── navbar.ejs
│   │   ├── footer.ejs
│   │   └── flash.ejs
│   ├── layouts/           # Layout templates
│   │   └── boilerplate.ejs
│   ├── listings/          # Listing pages
│   └── users/             # Authentication pages
│
├── 📂 public/             # Static assets
│   ├── css/              # Stylesheets
│   │   ├── style.css
│   │   └── rating.css
│   └── js/               # JavaScript files
│       ├── map.js
│       └── script.js
│
├── 📂 utils/             # Utility functions
│   ├── ExpressError.js
│   └── wrapAsync.js
│
├── 📂 init/              # Initialization scripts
│   ├── data.js
│   └── index.js
│
├── app.js               # Main application file
├── cloudConfig.js       # Cloudinary configuration
├── middleware.js        # Custom middleware
├── schema.js            # Joi validation schemas
└── package.json         # Dependencies
```

---

## 🎯 Key Features Explained

### 🔐 Secure Authentication
- Passport.js with local strategy
- Session-based authentication
- Secure password hashing
- Protected routes middleware

### 📸 Image Upload
- Multer for file handling
- Cloudinary for cloud storage
- Automatic image optimization
- Secure file validation

### 🗺️ Location Services
- Mapbox Geocoding API
- Interactive map display
- Property location markers
- Address to coordinates conversion

### ⭐ Review System
- 5-star rating system
- Text-based reviews
- User attribution
- Owner review management

---

## 🚧 API Endpoints

### Authentication
- `GET /signup` - Sign up page
- `POST /signup` - Create new user
- `GET /login` - Login page
- `POST /login` - User login
- `GET /logout` - User logout

### Listings
- `GET /listings` - View all listings
- `GET /listings/new` - Create listing form
- `POST /listings` - Create new listing
- `GET /listings/:id` - View single listing
- `GET /listings/:id/edit` - Edit listing form
- `PUT /listings/:id` - Update listing
- `DELETE /listings/:id` - Delete listing

### Reviews
- `POST /listings/:id/reviews` - Create review
- `DELETE /listings/:id/reviews/:reviewId` - Delete review

---

## 🎨 Design Features

- **Modern Color Palette** - Professional indigo/purple theme
- **Responsive Design** - Mobile-first approach
- **Smooth Animations** - Enhanced user experience
- **Clean Typography** - Plus Jakarta Sans font family
- **Glassmorphism Effects** - Modern UI elements
- **Gradient Backgrounds** - Visual appeal

---

## 🔒 Security Features

- ✅ Password hashing with Passport-Local-Mongoose
- ✅ Session management with MongoDB store
- ✅ CSRF protection
- ✅ Input validation with Joi
- ✅ Secure file upload validation
- ✅ Protected routes with middleware

---

## 📝 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `ATLASDB_URL` | MongoDB connection string | ✅ |
| `CLOUD_NAME` | Cloudinary cloud name | ✅ |
| `CLOUD_API_KEY` | Cloudinary API key | ✅ |
| `CLOUD_API_SECRET` | Cloudinary API secret | ✅ |
| `SECRET` | Session secret key | ✅ |
| `MAP_TOKEN` | Mapbox access token | ✅ |
| `NODE_ENV` | Environment (development/production) | ❌ |

---

## 🤝 Contributing

Contributions are welcome! If you'd like to contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Your Name**

- GitHub: [@abhiguptanitb](https://github.com/abhiguptanitb)
- LinkedIn: [abhiguptanitb](https://linkedin.com/in/abhiguptanitb)

---

## 🙏 Acknowledgments

- [Express.js](https://expressjs.com/) - Web framework
- [MongoDB](https://www.mongodb.com/) - Database
- [Cloudinary](https://cloudinary.com/) - Image management
- [Mapbox](https://www.mapbox.com/) - Maps and geocoding
- [Bootstrap](https://getbootstrap.com/) - CSS framework
- [Font Awesome](https://fontawesome.com/) - Icons

---

<div align="center">

**Made with ❤️ using Node.js and Express**

⭐ Star this repo if you find it helpful!

</div>
