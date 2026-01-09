# Webdev Strapi Backend

This is the Strapi backend for the Webdev website.It provides the API for managing projects and blog posts displayed on the frontend.

You can find the frontend React website [here](https://github.com/juhbence90/webdev-site-project-frontend).

![App Screenshot](./public/screen.png)

## ✨ Features

- REST API for Projects and Blog Posts
- Rich media upload support (via Strapi Media Library)
- Custom fields including image, tags, description, etc.
- Role-based admin panel
- Easily deployable to services like Render, Railway, or DigitalOcean

## 📦 Setup Instructions

Clone the repository and install dependencies:

## Setup & Usage

# 1. Clone the Repo
```bash
git clone https://github.com/juhbence90/webdev-site-project-backend.git
cd webdev-project-backend
```

# 2. Install dependencies

```bash
npm install
```

# 3. Configure Environment
Copy the example env file:

```bash
cp .env.example .env
```
Then update .env with your database connection and other required settings. Use a Neon PostgreSQL database. So you need to create an account at neon.com and then add your own database string.

# 4. Start the Server

```bash
npm run develop
```
This will launch Strapi in development mode at:
```bash
http://localhost:1337/admin
```

# 5. API Endpoints

Example public endpoints:
- /api/posts
- /api/projects

You can use query parameters for:
- Sorting: ?sort=date:desc
- Filtering: ?filters[category][$eq]=design
- Pagination: ?pagination[limit]=5
- Population: ?populate=image

Permissions
Make sure to allow public access to the required content types:
- Go to Settings > Roles > Public
- Enable find and findOne for post and project

Media Uploads
By default, media is stored locally under /public/uploads.
