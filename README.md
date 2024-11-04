# Ordering Food App Backend

Api for the ordering food app, to manage create, edit and update users, orders, and restaurants.

Created with [Express](https://expressjs.com/) and [MongoDB](https://www.mongodb.com/).

Authentication is done with [JWT](https://jwt.io/) and Auth0 for user management.

Orders payments are processed with [Stripe](https://stripe.com/).

Images are uploaded to [Cloudinary](https://cloudinary.com/) for storage.

## Features

- User management
- Order management
- Restaurant management
- Image uploading
- Payment processing

## Tech Stack

- Node.js
- Express
- MongoDB
- Mongoose
- JWT
- Stripe
- Cloudinary

## Installation

1. Clone the repo
2. Install dependencies
3. Create a `.env` file in the root directory and add the following variables:

```js
MONGODB_CONNECTION_STRING=mongodb+srv://<username>:<password>@cluster0.b9x9.mongodb.net/<dbname>?retryWrites=true&w=majority
STRIPE_WEBHOOK_SECRET=your-stripe-secret-webhook-key
STRIPE_API_KEY=your-stripe-api-key
CLOUDINARY_CLOUD_NAME=your-cloudinary-cloud-name
CLOUDINARY_API_KEY=your-cloudinary-api-key
CLOUDINARY_API_SECRET=your-cloudinary-api-secret
FRONTEND_URL=your-frontend-url
AUTH0_AUDIENCE=your-auth0-audience
AUTH0_ISSUER_BASE_URL=your-auth0-issuer-base-url
```

4. Run the server

```bash
npm run dev
```

5. Open your browser and go to `http://localhost:7000`

## Endpoints

### Users

#### Create User

`POST /api/my/user`

#### Get User

`GET /api/my/user/:id`

#### Update User

`PUT /api/my/user/:id`

### My Restaurant

#### Create Restaurant

`POST /api/my/restaurant`

#### Get Restaurant

`GET /api/my/restaurant`

#### Update Restaurant

`PUT /api/my/restaurant`

#### Get Restaurant Orders

`GET /api/my/restaurant/order`

#### Update Restaurant Orders Status

`PATCH /api/my/restaurant/order/:orderId/status`

### Restaurants

#### Search Restaurants by city

`GET /api/restaurant/search:city`

#### Get Restaurant

`GET /api/restaurant/:restaurantId`

### Orders

#### Get Orders

`GET /api/order`

#### Create Order and Checkout Session

`POST /api/order/checkout/create-checkout-session`

#### Webhook Handler

`POST /api/order/checkout/webhook`

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
