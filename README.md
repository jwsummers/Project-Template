# Project Template

This is a starter template for web development projects using React, Next.js, Tailwind CSS, Node.js, TypeScript, Prisma, and Docker.

## Getting Started

Follow these steps to set up the template for your project:

### 1. Clone the Repository

Clone the template repository to your local machine:

```bash
git clone https://github.com/yourusername/project-template.git
```

### 2. Install Dependencies

Navigate to the client and server directories and install the necessary packages.

For the client (frontend):

```bash
cd client
npm install
```

For the server (backend):

```bash
cd ../server
npm install
```

### 3. Setup Enviornment Variables

Copy the `.env.example` file to `.env` and update it with your database credentials:

```bash
cp .env.example .env
```

Edit the `.env` file to include your database connection details:

 ```plaintext
   DATABASE_URL=your-database-url
   API_KEY=your-api-key
   SECRET_KEY=your-secret-key
   ```

### 4. Initialize the Database (Optional)

If you're using Prisma for database management, set up your database and run the migrations.

Generate the Prisma client and apply the initial migration:

```bash
npx prisma migrate dev --name init
```

### 5. Start the Development Servers

You can start the client and server using Docker or by running the following commands separately:

Using Docker (Recommended):

```bash
docker-compose up --build
```

Manually:

Start the client:

```bash
cd client
npm run dev
```

Start the server:

```bash
cd ../server
npm run dev
```

### 6. Customize the `next.config.js`

The `next.config.js` file in the `client` directory is kept minimal. Customize it to suit your project's needs as you develop.

```javascript
/** @type {import('next').NextConfig} */
const nextConfig = {
  reactStrictMode: true,
  swcMinify: true,
};

module.exports = nextConfig;
```

Project Structure
Here's an overview of the project structure:

/project-template
├── client/               # Frontend - React, Next.js, Tailwind CSS
│   ├── public/           # Public assets
│   ├── src/              # Source files
│   │   ├── components/   # React components
│   │   ├── pages/        # Next.js pages
│   │   ├── styles/       # CSS/SASS files
│   │   └── index.tsx     # Main entry point
│   ├── next.config.js    # Next.js configuration
│   └── tailwind.config.js # Tailwind CSS configuration
├── server/               # Backend - Node.js, Express, Prisma
│   ├── prisma/           # Prisma schema and migrations
│   ├── src/              # Source files
│   │   ├── controllers/  # Express controllers
│   │   ├── models/       # Database models
│   │   ├── routes/       # Express routes
│   │   └── index.ts      # Main entry point
│   ├── Dockerfile        # Dockerfile for backend
│   ├── package.json      # NPM package file
│   └── tsconfig.json     # TypeScript configuration
├── .env.example          # Example environment variables file
├── docker-compose.yml    # Docker Compose configuration
└── README.md             # Project documentation


Customization
This template includes the basic setup for a full-stack application. Customize as needed:

Frontend (Client): React, Next.js, Tailwind CSS.
Backend (Server): Node.js, Express, Prisma with PostgreSQL.
Docker: Docker and Docker Compose for containerization.

License
This template is open-source and available under the MIT License. Feel free to use, modify, and distribute as needed.

