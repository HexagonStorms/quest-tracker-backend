# QuestTracker Backend

Node.js + Express backend for QuestTracker, handling task management and gamification logic.

## Tech Stack

- Node.js + Express
- TypeScript
- MongoDB Atlas
- Firebase Admin SDK
- Winston logging
- Jest testing

## Prerequisites

- Node.js >= 18
- Yarn
- MongoDB Atlas account
- Firebase project credentials
- WSL2 (Windows development)

## Setup

```zsh
yarn install
cp .env.example .env
# Configure environment variables
yarn dev
```

## API Structure

```
/api/v1/
├── /auth
│   ├── POST /register
│   ├── POST /login
│   └── POST /verify-token
├── /tasks
│   ├── GET /
│   ├── POST /
│   ├── PUT /:id
│   ├── DELETE /:id
│   └── PATCH /:id/complete
└── /users
    ├── GET /me
    ├── PATCH /me
    └── GET /me/stats
```

## Development

### Scripts
```zsh
yarn dev         # Development with hot reload
yarn build       # Build TypeScript
yarn start       # Run production build
yarn test        # Run tests
yarn lint        # Check code
```

### Project Structure

```
src/
├── config/      # App configuration
├── controllers/ # Route controllers
├── middleware/  # Express middleware
├── models/      # MongoDB models
├── routes/      # API routes
├── services/    # Business logic
├── types/       # TypeScript types
└── utils/       # Helper functions
```

### Environment Variables

```env
NODE_ENV=development
PORT=3000
MONGODB_URI=mongodb+srv://...
FIREBASE_PROJECT_ID=...
```

## Testing

```zsh
# Unit tests
yarn test

# Coverage report
yarn test --coverage

# Integration tests
yarn test:integration
```

## Monitoring

- Winston logging
- MongoDB Atlas monitoring
- Error tracking with Sentry
- Custom metrics collection

## Security

- JWT validation
- Rate limiting
- CORS configuration
- Request validation
- MongoDB encryption at rest

## License

0BSD