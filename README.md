# Shop Yangu Backend

A lightweight JSON Server backend for managing shops and their products. This project provides a RESTful API for a shop management system, perfect for e-commerce applications and small business inventory management.

## Features

- RESTful API endpoints for shops and products
- Sample data included with various shop categories
- Easy to extend and customize
- Built with JSON Server for rapid development
- Ready for deployment

## Getting Started

### Prerequisites

- Node.js (v12 or higher)
- npm (comes with Node.js)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/bridgitkanini/shop-yangu-backend.git
   cd shop-yangu-backend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

### Running the Server

Start the JSON Server:
```bash
npm start
```

The server will start on `http://localhost:3000` by default. If you want to specify a different port, set the PORT environment variable:

```bash
PORT=4000 npm start
```

## API Endpoints

### Shops

- `GET /shops` - Get all shops
- `GET /shops/:id` - Get a specific shop by ID
- `POST /shops` - Create a new shop
- `PUT /shops/:id` - Update a shop
- `DELETE /shops/:id` - Delete a shop

### Products

- `GET /shops/:shopId/products` - Get all products for a specific shop
- `GET /shops/:shopId/products/:productId` - Get a specific product from a shop
- `POST /shops/:shopId/products` - Add a new product to a shop
- `PUT /shops/:shopId/products/:productId` - Update a product
- `DELETE /shops/:shopId/products/:productId` - Delete a product

## Sample Data

The database comes pre-loaded with sample data including:

- Duka la Swahili (Traditional Swahili shop)
- Mboga Fresh (Local market for fresh produce)
- Mavazi Mazuri (Clothing store)
- Teknolojia Hapa (Electronics store)
- Vinywaji vya Asili (Fresh juice shop)

## Data Structure

### Shop
```typescript
{
  id: string;
  name: string;
  description: string;
  logo: string; // URL to shop logo
  products?: Product[]; // Array of products (optional)
}
```

### Product
```typescript
{
  id: number;
  name: string;
  price: number;
  stockLevel: number;
  description: string;
  image: string; // URL to product image
}
```

## Customization

To modify the data structure or add new endpoints, you can:

1. Edit the `db.json` file directly for data changes
2. Create a `routes.json` file to define custom routes
3. Create a `server.js` file to add custom middleware or additional endpoints

## Deployment

This application is currently deployed at: [https://shop-yangu-backend.onrender.com](https://shop-yangu-backend.onrender.com)

### Available Endpoints
- Shops: [https://shop-yangu-backend.onrender.com/shops](https://shop-yangu-backend.onrender.com/shops)
- Products: [https://shop-yangu-backend.onrender.com/shops/1/products](https://shop-yangu-backend.onrender.com/shops/1/products) (replace `1` with shop ID)

### Deployment Options
This application can be easily deployed to various services including:
- [Render](https://render.com/) (current deployment)
- [Heroku](https://www.heroku.com/)
- [Vercel](https://vercel.com/)
- [Railway](https://railway.app/)

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
