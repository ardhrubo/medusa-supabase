<<<<<<< HEAD
# Medusa With Supabase

=======
# Medusa E-Commerce Project

A full-featured e-commerce solution built with [Medusa](https://medusajs.com/), an open-source headless commerce engine, and a Next.js storefront.

## Project Structure

This project consists of two main components:

- `watchfire/` - The Medusa backend server
- `watchfire-storefront/` - The Next.js frontend application

## Prerequisites

- Node.js 16+
- PostgreSQL
- Redis (optional, recommended for production)

## Getting Started

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd watchfire
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   ```bash
   cp .env.example .env
   ```
   Edit the `.env` file with your database credentials and other configurations.

4. Run database migrations:
   ```bash
   npm run migrations
   ```

5. Seed the database (optional):
   ```bash
   npm run seed
   ```

6. Build the admin panel:
   ```bash
   npm run build
   ```

7. Start the Medusa server:
   ```bash
   npm run start
   ```
   The server will run on port 9000 by default.

### Storefront Setup

1. Navigate to the storefront directory:
   ```bash
   cd watchfire-storefront
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   ```bash
   cp .env.example .env.local
   ```
   Edit the `.env.local` file to connect to your Medusa backend.

4. Start the development server:
   ```bash
   npm run dev
   ```
   The storefront will run on port 8000 by default.

## Environment Variables

### Backend (watchfire)

Key environment variables for the backend:

- `DATABASE_URL`: PostgreSQL connection string
- `REDIS_URL`: Redis connection string (optional)
- `JWT_SECRET`: Secret for JWT tokens
- `COOKIE_SECRET`: Secret for cookies
- `PORT`: Server port (default: 9000)

See `.env.example` for a complete list of available options.

### Storefront (watchfire-storefront)

Key environment variables for the storefront:

- `MEDUSA_BACKEND_URL`: URL of the Medusa backend
- `NEXT_PUBLIC_MEDUSA_PUBLISHABLE_KEY`: Publishable API key from Medusa
- `NEXT_PUBLIC_DEFAULT_REGION`: Default region code

See `.env.example` for a complete list of available options.

## Features

- **Backend**:
  - RESTful API for products, orders, customers, etc.
  - Admin panel for store management
  - Extensible plugin system
  - Multi-region support
  - Flexible pricing
  - Inventory management

- **Storefront**:
  - Responsive design
  - Product browsing and filtering
  - Cart and checkout flow
  - Customer account management
  - Order history
  - Multi-currency support

## Development

### Extending the Backend

The Medusa backend can be extended with custom:

- API routes in `src/api/`
- Services in `src/services/`
- Subscribers in `src/subscribers/`
- Modules in `src/modules/`

### Customizing the Storefront

The Next.js storefront can be customized by modifying:

- Pages in `src/app/`
- Components in `src/modules/`
- Styles in `src/styles/`
- API calls in `src/lib/data/`

## Deployment

### Backend Deployment

The Medusa backend can be deployed to any Node.js hosting service:

1. Set up a PostgreSQL database
2. Configure environment variables
3. Build the admin panel with `npm run build`
4. Start the server with `npm run start`

### Storefront Deployment

The Next.js storefront can be deployed to Vercel, Netlify, or any other static site hosting:

1. Configure environment variables
2. Build the application with `npm run build`
3. Deploy the generated output

## Troubleshooting

### Common Issues

- **Backend not starting**: Ensure that your database is running and the connection details are correct in `.env`
- **JSON parsing errors in middleware**: Check that your Medusa server is running and accessible
- **XML responses instead of JSON**: Verify your API key and CORS settings
- **Missing admin panel**: Run `npm run build` in the backend directory

## Resources

- [Medusa Documentation](https://docs.medusajs.com/)
- [Next.js Documentation](https://nextjs.org/docs)

## License

This project is licensed under the [MIT License](LICENSE).
>>>>>>> 8529a25 (chore: update README with project details, setup instructions, and features)
