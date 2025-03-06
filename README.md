# Airbnb Clone

This project is a clone of the popular vacation rental platform, Airbnb. It allows users to create, view, edit, and delete listings, as well as leave reviews for listings. The project is built using Node.js, Express, MongoDB, and EJS for templating.

## Features

- User authentication and authorization
- Create, read, update, and delete listings
- Upload images for listings using Cloudinary
- Leave reviews for listings
- Flash messages for user feedback
- Responsive design

## Technologies Used

- Node.js
- Express
- MongoDB
- Mongoose
- EJS
- Passport.js (for authentication)
- Cloudinary (for image uploads)
- Connect-flash (for flash messages)
- Express-session (for session management)
- Joi (for data validation)

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/Major-Project-Airbnb-.git
   cd Major-Project-Airbnb-
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add the following environment variables:
   ```env
   CLOUD_NAME=your_cloudinary_cloud_name
   CLOUD_API_KEY=your_cloudinary_api_key
   CLOUD_API_SECRET=your_cloudinary_api_secret
   ATLASDB_URL=your_mongodb_atlas_url
   SECRET=your_session_secret
   ```

4. Start the server:
   ```sh
   npm start
   ```

5. Open your browser and navigate to `http://localhost:8080`.

## Usage

### User Authentication

- Sign up for a new account
- Log in to your account
- Log out of your account

### Listings

- View all listings
- Create a new listing (must be logged in)
- Edit your own listings (must be logged in and be the owner)
- Delete your own listings (must be logged in and be the owner)

### Reviews

- Leave a review on a listing (must be logged in)
- Edit your own reviews (must be logged in and be the author)
- Delete your own reviews (must be logged in and be the author)

## Folder Structure

```
.
├── controllers
│   ├── listings.js
│   ├── reviews.js
│   └── user.js
├── init
│   ├── data.js
│   └── index.js
├── models
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── public
│   ├── css
│   │   ├── rating.css
│   │   └── style.css
│   ├── js
│   │   ├── map.js
│   │   └── script.js
├── routes
│   ├── listing.js
│   ├── review.js
│   └── user.js
├── utils
│   ├── ExpressError.js
│   └── wrapAsync.js
├── views
│   ├── includes
│   │   ├── flash.ejs
│   │   ├── footer.ejs
│   │   ├── navbar.ejs
│   ├── layouts
│   │   └── boilerplate.ejs
│   ├── listings
│   │   ├── edit.ejs
│   │   ├── index.ejs
│   │   ├── new.ejs
│   │   └── show.ejs
│   ├── users
│   │   ├── login.ejs
│   │   └── signup.ejs
│   └── error.ejs
├── .env
├── .gitignore
├── app.js
├── cloudConfig.js
├── middleware.js
├── package.json
├── package-lock.json
└── README.md
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request if you have any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
