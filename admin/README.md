# E-Commerce Admin Panel

This is the admin panel for the e-commerce application, built with React and Vite. It provides administrators with tools to manage products, orders, and other store operations.

## Features

- **Product Management**: Add, edit, and remove products from the store catalog
- **Order Management**: View and process customer orders
- **Admin Authentication**: Secure login system for administrators
- **Dashboard**: Overview of store statistics and recent activities
- **Responsive Design**: Works on desktop and mobile devices

## Tech Stack

- **Frontend**: React 18 with Vite
- **Styling**: Tailwind CSS for responsive design
- **Icons**: Custom icons and assets
- **Build Tool**: Vite for fast development and optimized builds
- **Linting**: ESLint for code quality

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager

### Installation

1. Navigate to the admin directory:
   ```bash
   cd admin
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to the provided localhost URL (usually http://localhost:5173)

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Project Structure

```
admin/
├── src/
│   ├── components/     # Reusable UI components
│   ├── pages/         # Page components for different routes
│   ├── assets/        # Images, icons, and static assets
│   ├── App.jsx        # Main application component
│   └── main.jsx       # Application entry point
├── public/            # Static files
└── package.json       # Dependencies and scripts
```

## Development

The admin panel is configured to work with the backend API. Ensure the backend server is running on the specified port for full functionality.

## Contributing

When adding new features or making changes:
1. Create a new branch for your feature
2. Make your changes
3. Test thoroughly
4. Submit a pull request
