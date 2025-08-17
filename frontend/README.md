# 🛍️ Ecommerce App

A modern, responsive ecommerce application built with React, Vite, and Tailwind CSS.

## 🚀 Features

- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **Product Catalog** - Browse products with filtering and search functionality
- **Shopping Cart** - Add/remove items with quantity management
- **User Authentication** - Login/register system for customers
- **Order Management** - Track orders and order history
- **Payment Integration** - Secure checkout with payment processing
- **Admin Dashboard** - Manage products, orders, and inventory
- **Modern UI/UX** - Clean, intuitive interface with smooth animations

## 🛠️ Tech Stack

- **Frontend Framework:** React 18
- **Build Tool:** Vite
- **Styling:** Tailwind CSS
- **State Management:** React Context API
- **Routing:** React Router
- **Icons:** React Icons
- **HTTP Client:** Axios
- **Payment:** Razorpay & Stripe integration

## 📁 Project Structure

```
frontend/
├── public/              # Static assets
├── src/
│   ├── components/      # Reusable UI components
│   ├── pages/          # Page components
│   ├── context/        # React Context providers
│   ├── assets/         # Images and static files
│   ├── App.jsx         # Main application component
│   └── main.jsx        # Application entry point
├── package.json        # Dependencies and scripts
└── README.md          # This file
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. **Clone the repository**

   ```bash
   git clone [your-repo-url]
   cd ecommerce-app/frontend
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Start the development server**

   ```bash
   npm run dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## 🎯 Key Pages

- **Home** - Featured products and hero section
- **Collection** - Browse all products with filters
- **Product Details** - Individual product page with reviews
- **Cart** - Shopping cart with checkout
- **Login/Register** - User authentication
- **Orders** - Order history and tracking
- **About** - Company information
- **Contact** - Contact form and support

## 🔧 Development

### Environment Variables

Create a `.env` file in the frontend directory:

```env
VITE_API_URL=http://localhost:3000/api
VITE_RAZORPAY_KEY=your_razorpay_key
VITE_STRIPE_KEY=your_stripe_key
```

### API Integration

The frontend connects to a backend API (not included in this repo). Make sure your backend server is running on the specified port.

## 🎨 Customization

- **Colors:** Modify `tailwind.config.js`
- **Fonts:** Update `index.css` and `tailwind.config.js`
- **Components:** All components are in `src/components/`
- **Pages:** All pages are in `src/pages/`

## 📱 Responsive Design

The application uses Tailwind CSS's responsive utilities:

- **Mobile:** < 768px
- **Tablet:** 768px - 1024px
- **Desktop:** > 1024px

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- React team for the amazing framework
- Tailwind CSS for the utility-first styling
- Vite for the fast build tool
- All contributors and supporters

---

**Happy coding!** 🎉
