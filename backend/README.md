# 🚀 E-Commerce Backend API

A robust, scalable RESTful API built with Node.js and Express for a modern e-commerce platform.

## 🛠️ Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT (JSON Web Tokens)
- **File Upload**: Multer with Cloudinary integration
- **Validation**: Express-validator
- **Security**: Helmet, CORS, Rate limiting
- **Environment**: dotenv for configuration management

## 📁 Project Structure

```
backend/
├── config/              # Database and cloud configuration
├── controllers/         # Business logic for each route
├── middleware/          # Authentication and validation middleware
├── models/             # MongoDB schemas and models
├── routes/             # API route definitions
├── uploads/            # Temporary file storage
├── server.js           # Application entry point
└── package.json        # Dependencies and scripts
```

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- MongoDB (local or cloud instance)
- Cloudinary account (for image storage)

### Installation

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Set up environment variables**
   Create a `.env` file in the backend directory:
   ```env
   PORT=4000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   CLOUDINARY_NAME=your_cloudinary_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_SECRET_KEY=your_cloudinary_secret_key
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```

## 📡 API Endpoints

### **Authentication Routes**
- `POST /api/user/register` - User registration
- `POST /api/user/login` - User login
- `POST /api/user/admin` - Admin login

### **Product Routes**
- `GET /api/product/list` - Get all products
- `GET /api/product/single/:id` - Get single product
- `POST /api/product/add` - Add new product (Admin only)
- `PUT /api/product/update/:id` - Update product (Admin only)
- `DELETE /api/product/remove/:id` - Delete product (Admin only)

### **Cart Routes**
- `POST /api/cart/add` - Add item to cart
- `POST /api/cart/remove` - Remove item from cart
- `POST /api/cart/get` - Get user cart
- `POST /api/cart/update` - Update cart quantity

### **Order Routes**
- `POST /api/order/place` - Place new order
- `POST /api/order/userorders` - Get user orders
- `POST /api/order/list` - Get all orders (Admin only)
- `POST /api/order/status` - Update order status (Admin only)

## 🔐 Authentication & Authorization

### **JWT Token Structure**
- **Access Token**: 15-minute expiry for API access
- **Refresh Token**: 7-day expiry for token renewal

### **Role-Based Access Control**
- **User**: Standard customer access
- **Admin**: Full administrative privileges

### **Protected Routes**
- All cart operations require authentication
- All order operations require authentication
- Product management requires admin role
- Order management requires admin role

## 🗄️ Database Schema

### **User Model**
```javascript
{
  name: String (required),
  email: String (unique, required),
  password: String (hashed, required),
  cartData: Object,
  role: String (default: 'user')
}
```

### **Product Model**
```javascript
{
  name: String (required),
  description: String,
  price: Number (required),
  category: String (required),
  image: Array,
  sizes: Array,
  bestseller: Boolean,
  date: Date (default: Date.now)
}
```

### **Order Model**
```javascript
{
  userId: ObjectId (ref: User),
  items: Array (required),
  amount: Number (required),
  address: Object (required),
  status: String (default: 'Pending'),
  date: Date (default: Date.now),
  payment: Boolean (default: false)
}
```

## 🛡️ Security Features

- **Password Hashing**: bcrypt with salt rounds
- **JWT Token**: Secure token generation and validation
- **Input Validation**: Express-validator for all inputs
- **Rate Limiting**: API rate limiting to prevent abuse
- **CORS**: Configured for cross-origin requests
- **Helmet**: Security headers protection

## 🚀 Performance Optimizations

- **Database Indexing**: Optimized queries with proper indexing
- **Image Optimization**: Cloudinary for efficient image delivery
- **Response Compression**: Gzip compression enabled
- **Caching**: Redis-ready architecture
- **Pagination**: Efficient data fetching for large datasets

## 🧪 Testing

### **Manual Testing**
- Postman collection available for API testing
- Test user credentials provided in documentation
- Sample data for testing cart and order flows

### **Test Commands**
```bash
npm test          # Run test suite
npm run test:watch # Run tests in watch mode
```

## 📊 Monitoring & Logging

- **Request Logging**: Morgan for HTTP request logs
- **Error Handling**: Centralized error handling middleware
- **Health Check**: `/health` endpoint for monitoring
- **Performance Metrics**: Response time tracking

## 🔄 API Response Format

### **Success Response**
```json
{
  "success": true,
  "data": { ... },
  "message": "Operation successful"
}
```

### **Error Response**
```json
{
  "success": false,
  "message": "Error description",
  "error": { ... }
}
```

## 🚀 Deployment

### **Environment Variables for Production**
```env
NODE_ENV=production
PORT=4000
MONGODB_URI=production_mongodb_uri
JWT_SECRET=strong_jwt_secret
CLOUDINARY_NAME=production_cloudinary
CLOUDINARY_API_KEY=production_api_key
CLOUDINARY_SECRET_KEY=production_secret_key
```

### **Build & Deploy**
```bash
npm run build
npm start
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch: `git checkout -b feature/new-feature`
3. Commit changes: `git commit -m 'Add new feature'`
4. Push to branch: `git push origin feature/new-feature`
5. Submit pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support, email: [your-email] or create an issue in the GitHub repository.
