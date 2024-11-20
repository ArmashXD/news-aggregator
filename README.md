# News Aggregator

News Aggregator is a full-stack web application that collects, filters, and displays articles from multiple news sources. The app allows users to search and filter articles based on various criteria and manage their news preferences.

## Features

### Frontend

- Built with **React** and **Tailwind CSS** and **ShadCn**.
- Real-time search and filtering options for articles.
- Infinite scrolling for seamless browsing.
- Multi-select filters for authors, categories, and sources.
- Responsive design for mobile, tablet, and desktop.

### Backend

- Built with **Laravel**.
- Supports **cursor-based pagination** for efficient data handling.
- Provides a robust API for managing articles and user preferences.
- Queue management for background tasks using **Laravel Queue**.
- Scheduled commands for periodic operations.

### Database

- Uses **MySQL** as the relational database for managing articles, preferences, and user data.

---

## Technologies Used

### Frontend

- **React**: JavaScript library for building user interfaces.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **Redux**: State management library.
- **React Infinite Scroll Component**: For infinite scrolling functionality.

### Backend

- **Laravel**: PHP framework for backend development.
- **MySQL**: Relational database for storing data.
- **Docker**: Containerization for consistent development and deployment environments.

---

## Requirements

Ensure you have the following installed on your machine:

- **Docker** and **Docker Compose**
- **Node.js** (>= 18.x)
- **npm** or **yarn** (for frontend dependencies)
- **MySQL** (optional if using Docker)

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/ArmashXD/news-aggregator
cd news-aggregator
```

### 2. Environment Variables

- Create a .env file in the backend directory and configure it as follows

```bash
APP_KEY=
APP_ENV=local
APP_DEBUG=true
DB_CONNECTION=mysql
DB_HOST=db
DB_PORT=3306
DB_DATABASE=news
DB_USERNAME=user
DB_PASSWORD=password
QUEUE_CONNECTION=database
```

- Create a .env file in the frontend directory for any frontend-specific configurations (optional).

### 3. Start Services:

Run the following command to build and start the containers

```bash
docker-compose up --build
```

### 4. Access the Application:

```bash
Frontend: http://localhost:3000
Backend: http://localhost:8000
```

### 5. Running Artisan Commands in Backend

To run Laravel artisan commands, access the backend container:

```bash
docker exec -it laravel-backend bash
php artisan migrate
php artisan queue:work
```

### Key Features in Detail

- Article Search and Filtering
- Users can search and filter articles by:

### Keywords

- Authors (multi-select)
- Categories (multi-select)
- Sources (multi-select)
- Date (filter by specific date)
- Infinite Scrolling
- Articles are displayed with infinite scrolling to enhance user experience and performance.

### User Preferences

- Users can set their preferences for:

### Favorite authors, categories, and sources.

- These preferences are saved and applied to the news feed

### Development

Running Locally Without Docker

### Backend

```bash
cd backend
composer install
php artisan serve

```

### Frontend

```bash
cd frontend
npm install
npm run dev


```
