# Hotel Listings

A full-stack web application for browsing and reviewing hotel listings built with Node.js, Express, MongoDB, and EJS.

## Features

- User authentication (signup/login) using Passport local strategy
- Create, edit, delete hotel listings
- Add and delete reviews on listings
- Flash messages for success/error UX
- Server-side validation with Express middleware
- Session-backed login state persistence using MongoDB
- Responsive UI with EJS templates and CSS
- Map integration via frontend `map.js` (OpenStreetMap / Leaflet style)

## Tech Stack

- Node.js
- Express
- MongoDB with Mongoose
- EJS (templating)
- Passport.js for auth
- connect-mongo for session store
- dotenv for environment variables

## Project Structure

- `app.js` - main application file
- `controllers/` - request handlers:
  - `listing.js`
  - `review.js`
  - `user.js`
- `models/` - Mongoose schemas:
  - `listing.js`
  - `review.js`
  - `user.js`
- `routes/` - routes for listings, reviews, users
- `views/` - EJS templates and partials
- `public/` - static assets (CSS, JS)
- `utils/` - custom error and async utilities
- `init/` - seed/demo data loader (optional)
- `cloudConfig.js` - cloud DB or config logic (if present)

## Prerequisites

- Node.js >= 18
- npm
- MongoDB (Atlas connection string or local instance)

## Setup

1. Clone the repo

```bash
git clone <repo-url>
cd "Hotel Listings"
```

2. Install packages

```bash
npm install
```

3. Create a `.env` file in project root with:

```env
NODE_ENV=development
ATLASDB_URL=<your-mongo-url>
SECRET=<session-secret>
```

4. Run the application

```bash
npm start
```

5. Open in browser:

- `http://localhost:4040`

## Development

- Run nodemon (if installed)

```bash
npx nodemon app.js
```

## Seed data

- Use `init` folder items or add a demo route `/demouser` for quick user creation.

## Authentication

- Signup route: `/signup`
- Login route: `/login`
- Logout route: `/logout`

## Error handling

- Custom `ExpressError` middleware handles 404 and server errors and renders `views/error.ejs`.

## Customization

- Add city/hotel data in `models/listing.js` and adjust UI templates under `views/listings`.
- Change layout in `views/layouts/boilerplate.ejs`.

## License

MIT
