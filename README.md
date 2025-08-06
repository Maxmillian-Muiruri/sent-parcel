# SendIT - Parcel Delivery Management System

<div align="center">

![SendIT Logo](https://img.shields.io/badge/SendIT-Parcel%20Delivery-blue?style=for-the-badge&logo=package)

**A comprehensive, full-stack parcel delivery management system built with modern web technologies**

[![Angular](https://img.shields.io/badge/Angular-20-red?style=flat-square&logo=angular)](https://angular.io/)
[![NestJS](https://img.shields.io/badge/NestJS-10-ea2845?style=flat-square&logo=nestjs)](https://nestjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-336791?style=flat-square&logo=postgresql)](https://www.postgresql.org/)
[![Prisma](https://img.shields.io/badge/Prisma-6.12-2D3748?style=flat-square&logo=prisma)](https://www.prisma.io/)

[Live Demo](https://send-it-mauve.vercel.app) • [API Documentation](https://sendit-backend.onrender.com) • [Report Bug](https://github.com/Maxmillian-Muiruri/Send-IT/issues)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Getting Started](#-getting-started)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [API Documentation](#-api-documentation)
- [Database Schema](#-database-schema)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)
- [Folder Structure](#-folder-structure)

---

## 🚀 Overview

**SendIT** is a modern, full-stack parcel delivery management system designed to streamline the entire parcel delivery process. From parcel creation to final delivery, SendIT provides real-time tracking, automated notifications, and comprehensive management tools for users, couriers, and administrators.

### 🎯 Key Objectives

- **Efficient Parcel Management**: Streamline parcel creation, tracking, and delivery processes
- **Real-time Communication**: Provide instant updates via WebSocket connections and email notifications
- **Role-based Access Control**: Separate interfaces and permissions for users, couriers, and administrators
- **Location Intelligence**: Integrate Google Maps for accurate geocoding, routing, and tracking
- **Scalable Architecture**: Built with modern technologies for high performance and scalability

---

## ✨ Features

### 👤 **User Features**

- 🔐 **Secure Authentication** - JWT-based login/registration system
- 📦 **Parcel Creation** - Easy-to-use forms with address validation
- 💰 **Dynamic Pricing** - Automatic cost calculation based on distance and weight
- 📍 **Real-time Tracking** - Live parcel status and location updates
- 🔔 **Multi-channel Notifications** - Email and in-app notifications
- 📊 **Personal Dashboard** - Comprehensive view of sent/received parcels
- 🗺️ **Interactive Maps** - Google Maps integration for route visualization

### 🚚 **Courier Features**

- 📱 **Mobile-friendly Dashboard** - Optimized interface for delivery personnel
- 📋 **Delivery Management** - View and manage assigned parcels
- 📍 **Location Updates** - Real-time location sharing with customers
- ✅ **Status Management** - Update parcel status throughout delivery process
- 📈 **Performance Analytics** - Track delivery statistics and ratings

### 👨‍💼 **Admin Features**

- 🎛️ **Comprehensive Dashboard** - Full system overview and management
- 👥 **User Management** - Create, edit, and manage user accounts
- 🚚 **Courier Assignment** - Assign parcels to available couriers
- 📊 **Analytics & Reporting** - System-wide statistics and insights
- ⚙️ **System Configuration** - Manage pricing, settings, and notifications

### 🔧 **Technical Features**

- ⚡ **Real-time Updates** - WebSocket-based live communication
- 🗺️ **Google Maps Integration** - Professional mapping and geocoding
- 📧 **Email System** - Automated HTML email notifications
- 🔒 **Security** - JWT authentication, role-based access control
- 📱 **Responsive Design** - Works seamlessly on all devices
- 🚀 **Production Ready** - Deployed on Vercel and Render

---

## 🛠️ Tech Stack

### **Frontend**

- **Framework**: Angular 20
- **Language**: TypeScript 5.8
- **Styling**: CSS3 with custom components
- **Maps**: Google Maps API with @angular/google-maps
- **HTTP Client**: Angular HttpClient with interceptors
- **State Management**: RxJS Observables
- **Build Tool**: Angular CLI with Webpack

### **Backend**

- **Framework**: NestJS 11
- **Language**: TypeScript 5.7
- **Database**: PostgreSQL 16
- **ORM**: Prisma 6.12
- **Authentication**: JWT with Passport.js
- **Real-time**: Socket.io WebSockets
- **Email**: Nodemailer with HTML templates
- **Validation**: class-validator & class-transformer

### **Infrastructure & DevOps**

- **Frontend Hosting**: Vercel
- **Backend Hosting**: Render
- **Database**: Neon PostgreSQL (Cloud)
- **Maps**: Google Maps Platform
- **Version Control**: Git & GitHub
- **Package Manager**: npm

### **Development Tools**

- **Code Quality**: ESLint, Prettier
- **Testing**: Jest (Backend), Jasmine/Karma (Frontend)
- **API Testing**: REST Client files
- **Database Management**: Prisma Studio
- **Environment**: Node.js 18+

---

## 🏗️ Architecture

SendIT follows a modern **microservices-inspired architecture** with clear separation of concerns:

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │    Backend      │    │   External      │
│   (Angular)     │◄──►│   (NestJS)      │◄──►│   Services      │
│                 │    │                 │    │                 │
│ • Components    │    │ • Controllers   │    │ • Google Maps   │
│ • Services      │    │ • Services      │    │ • Email Service │
│ • Guards        │    │ • WebSocket     │    │ • Neon DB       │
│ • Interceptors  │    │ • Prisma ORM    │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

### **Key Architectural Patterns**

1. **Modular Design**: Both frontend and backend are organized into feature modules
2. **Dependency Injection**: NestJS and Angular's DI systems for loose coupling
3. **Repository Pattern**: Prisma ORM abstracts database operations
4. **Observer Pattern**: RxJS for reactive programming and real-time updates
5. **Guard Pattern**: Authentication and authorization guards
6. **Interceptor Pattern**: HTTP request/response transformation
7. **Gateway Pattern**: WebSocket communication for real-time features

---

## 🚀 Getting Started

### **Prerequisites**

Before running SendIT, ensure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** (v9 or higher)
- **PostgreSQL** (v14 or higher)
- **Git**

### **Quick Start**

1. **Clone the repository**

   ```bash
   git clone https://github.com/Maxmillian-Muiruri/Send-IT.git
   cd Send-IT
   ```

2. **Install dependencies**

   ```bash
   # Install backend dependencies
   cd sendit-backend
   npm install

   # Install frontend dependencies
   cd ../sendit-frontend
   npm install
   ```

3. **Set up environment variables**

   ```bash
   # Backend (.env)
   cp .env.example .env
   # Edit .env with your configuration

   # Frontend (environment.ts)
   # Update API URL and Google Maps key
   ```

4. **Set up database**

   ```bash
   cd sendit-backend
   npx prisma migrate dev
   npx prisma generate
   ```

5. **Start the applications**

   ```bash
   # Terminal 1 - Backend
   cd sendit-backend
   npm run start:dev

   # Terminal 2 - Frontend
   cd sendit-frontend
   npm start
   ```

6. **Access the application**
   - Frontend: http://localhost:4200
   - Backend API: http://localhost:3000

---

## 📦 Installation

### **Backend Setup**

1. **Navigate to backend directory**

   ```bash
   cd sendit-backend
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Environment Configuration**
   Create a `.env` file in the backend root:

   ```env
   # Database
   DATABASE_URL="postgresql://username:password@localhost:5432/sendit_db"

   # JWT
   JWT_SECRET="your-super-secret-jwt-key"

   # Google Maps
   GOOGLE_MAPS_API_KEY="your-google-maps-api-key"

   # Email Configuration
   MAIL_HOST="smtp.gmail.com"
   MAIL_PORT=587
   MAIL_USER="your-email@gmail.com"
   MAIL_PASS="your-app-password"
   MAIL_FROM="SendIT <noreply@sendit.com>"
   ```

4. **Database Setup**

   ```bash
   # Run migrations
   npx prisma migrate dev --name init

   # Generate Prisma client
   npx prisma generate

   # Seed database (optional)
   npm run seed
   ```

5. **Start development server**
   ```bash
   npm run start:dev
   ```

### **Frontend Setup**

1. **Navigate to frontend directory**

   ```bash
   cd sendit-frontend
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Environment Configuration**
   Update `src/environments/environment.ts`:

   ```typescript
   export const environment = {
     production: false,
     apiUrl: "http://localhost:3000",
     googleMapsApiKey: "your-google-maps-api-key",
   };
   ```

4. **Start development server**
   ```bash
   npm start
   ```

---

## 📖 Usage

### **User Journey**

1. **Registration & Login**

   - Visit the application homepage
   - Click "Sign Up" to create a new account
   - Choose user role (USER, COURIER, or ADMIN)
   - Login with credentials

2. **Sending a Parcel**

   - Navigate to "Send Parcel" from user dashboard
   - Fill in receiver details and parcel information
   - Enter pickup and delivery addresses
   - Review pricing and confirm shipment
   - Receive tracking code via email

3. **Tracking a Parcel**
   - Use "Track Parcel" feature with tracking code
   - View real-time status updates
   - See courier location on map
   - Receive notifications for status changes

### **Role-based Access**

#### **Regular Users**

- Send and receive parcels
- Track parcel status and location
- Manage personal profile
- View delivery history

#### **Couriers**

- View assigned deliveries
- Update parcel status
- Share real-time location
- Manage delivery schedule

#### **Administrators**

- Manage all users and parcels
- Assign couriers to deliveries
- View system analytics
- Configure system settings

---

## 📚 API Documentation

### **Authentication Endpoints**

```http
POST /auth/login
POST /auth/register
POST /auth/request-password-reset
POST /auth/reset-password
```

### **User Management**

```http
GET    /user                    # Get all users (Admin only)
POST   /user/register          # Register new user
GET    /user/profile           # Get user profile
PUT    /user/profile           # Update user profile
DELETE /user/:id               # Delete user (Admin only)
```

### **Parcel Management**

```http
GET    /parcel                 # Get parcels (filtered by user role)
POST   /parcel                 # Create new parcel
POST   /parcel/comprehensive   # Create parcel with addresses
GET    /parcel/:id             # Get parcel by ID
PUT    /parcel/:id             # Update parcel
DELETE /parcel/:id             # Delete parcel
PUT    /parcel/:id/status      # Update parcel status
PUT    /parcel/:id/assign-courier # Assign courier to parcel
```

### **Courier Management**

```http
GET    /courier                # Get all couriers
POST   /courier                # Create courier profile
GET    /courier/profile        # Get courier profile
PUT    /courier/profile        # Update courier profile
PUT    /courier/location       # Update courier location
GET    /courier/analytics      # Get courier analytics
```

### **Notifications**

```http
GET    /notifications          # Get user notifications
GET    /notifications/unread-count # Get unread count
PATCH  /notifications/:id/read # Mark notification as read
PATCH  /notifications/mark-all-read # Mark all as read
DELETE /notifications/:id      # Delete notification
```

### **Common Services**

```http
POST   /common/geocoding/forward  # Forward geocoding
GET    /common/geocoding/reverse  # Reverse geocoding
POST   /common/pricing/calculate  # Calculate pricing
GET    /common/analytics         # System analytics
```

### **WebSocket Events**

```javascript
// Client to Server
socket.emit("trackParcel", { parcelId: "parcel-id" });
socket.emit("updateLocation", {
  courierId: "courier-id",
  parcelId: "parcel-id",
  latitude: -1.286389,
  longitude: 36.817223,
});

// Server to Client
socket.on("statusUpdated", (data) => {
  // Handle status update
});
socket.on("locationUpdated", (data) => {
  // Handle location update
});
```

---

## 🗄️ Database Schema

### **Core Entities**

#### **User**

```sql
model User {
  id                      String    @id @default(uuid())
  email                   String    @unique
  password                String
  name                    String
  phone                   String?
  role                    UserRole  @default(USER)
  resetPasswordCode       String?
  resetPasswordCodeExpiry DateTime?
  createdAt               DateTime  @default(now())
  updatedAt               DateTime  @updatedAt

  // Relations
  sentParcels             Parcel[]  @relation("SentParcels")
  receivedParcels         Parcel[]  @relation("ReceivedParcels")
  notifications           Notification[]
  courierProfile          Courier?
  addresses               Address[]
}
```

#### **Parcel**

```sql
model Parcel {
  id                    String       @id @default(uuid())
  trackingCode          String       @unique
  description           String?
  weight                Float?
  status                ParcelStatus @default(PENDING)
  baseRate              Float        @default(5.0)
  weightCharge          Float        @default(0.0)
  distanceCharge        Float        @default(0.0)
  totalCost             Float        @default(0.0)
  distanceKm            Float        @default(0.0)
  estimatedDeliveryTime Int?
  createdAt             DateTime     @default(now())
  updatedAt             DateTime     @updatedAt

  // Relations
  sender                User         @relation("SentParcels")
  receiver              User         @relation("ReceivedParcels")
  courier               Courier?
  pickupAddress         Address?     @relation("PickupAddress")
  deliveryAddress       Address?     @relation("DeliveryAddress")
  statusHistory         ParcelStatusHistory[]
  notifications         Notification[]
}
```

#### **Courier**

```sql
model Courier {
  id              String        @id @default(uuid())
  user            User          @relation(fields: [userId], references: [id])
  userId          String        @unique
  vehicleType     String?
  licensePlate    String?
  locationLat     Float?
  locationLng     Float?
  currentLocation String?
  status          CourierStatus @default(AVAILABLE)
  isActive        Boolean       @default(true)
  createdAt       DateTime      @default(now())
  updatedAt       DateTime      @updatedAt

  // Relations
  assignedParcels Parcel[]
  notifications   Notification[]
}
```

### **Enums**

```sql
enum UserRole {
  USER
  ADMIN
  COURIER
}

enum ParcelStatus {
  PENDING
  PICKED_UP
  IN_TRANSIT
  OUT_FOR_DELIVERY
  DELIVERED
  CANCELLED
  RETURNED
}

enum CourierStatus {
  AVAILABLE
  BUSY
  OFFLINE
  ON_DELIVERY
}

enum NotificationType {
  PARCEL_CREATED
  PARCEL_ASSIGNED
  PARCEL_PICKED_UP
  PARCEL_IN_TRANSIT
  PARCEL_DELIVERED
  PARCEL_CANCELLED
  COURIER_NEARBY
  DELIVERY_UPDATE
  SYSTEM_ALERT
  PAYMENT_RECEIVED
  PAYMENT_FAILED
}
```

---

## 🚀 Deployment

### **Production Deployment**

SendIT is configured for deployment on modern cloud platforms:

#### **Frontend (Vercel)**

1. Connect GitHub repository to Vercel
2. Set build command: `npm run build:vercel`
3. Set output directory: `dist/sendit-frontend`
4. Configure environment variables
5. Deploy automatically on push to main branch

#### **Backend (Render)**

1. Connect GitHub repository to Render
2. Set build command: `npm install && npx prisma generate && npm run build`
3. Set start command: `npm run start:prod`
4. Configure environment variables
5. Deploy automatically on push to main branch

#### **Database (Neon)**

1. Create Neon PostgreSQL database
2. Get connection string
3. Run migrations: `npx prisma migrate deploy`
4. Generate Prisma client: `npx prisma generate`

### **Environment Variables for Production**

#### **Backend (Render)**

```env
NODE_ENV=production
DATABASE_URL=postgresql://user:pass@host.neon.tech/db
JWT_SECRET=your-production-jwt-secret
GOOGLE_MAPS_API_KEY=your-google-maps-api-key
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USER=your-email@gmail.com
MAIL_PASS=your-app-password
```

#### **Frontend (Vercel)**

```env
GOOGLE_MAPS_API_KEY=your-google-maps-api-key
```

### **Deployment Commands**

```bash
# Backend deployment
npm run build
npm run start:prod

# Frontend deployment
npm run build:vercel

# Database migration
npx prisma migrate deploy
npx prisma generate
```

---

## 🤝 Contributing

We welcome contributions to SendIT! Here's how you can help:

### **Getting Started**

1. **Fork the repository**

   ```bash
   git clone https://github.com/your-username/Send-IT.git
   cd Send-IT
   ```

2. **Create a feature branch**

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**

   - Follow the existing code style
   - Add tests for new features
   - Update documentation as needed

4. **Test your changes**

   ```bash
   # Backend tests
   cd sendit-backend
   npm run test

   # Frontend tests
   cd sendit-frontend
   npm run test
   ```

5. **Commit and push**

   ```bash
   git add .
   git commit -m "feat: add your feature description"
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request**
   - Describe your changes
   - Link any related issues
   - Wait for review and approval

### **Development Guidelines**

- **Code Style**: Follow TypeScript and Angular style guides
- **Commits**: Use conventional commit messages
- **Testing**: Write tests for new features and bug fixes
- **Documentation**: Update README and code comments
- **Performance**: Consider performance implications of changes

### **Reporting Issues**

- Use GitHub Issues to report bugs
- Provide detailed reproduction steps
- Include environment information
- Add screenshots for UI issues

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

### **MIT License Summary**

- ✅ **Commercial use** - Use for commercial purposes
- ✅ **Modification** - Modify the source code
- ✅ **Distribution** - Distribute the software
- ✅ **Private use** - Use privately
- ❌ **Liability** - No liability for damages
- ❌ **Warranty** - No warranty provided

---

## 📁 Folder Structure

```
Send-IT/
├── 📁 sendit-backend/                 # NestJS Backend Application
│   ├── 📁 src/
│   │   ├── 📁 address/                # Address management module
│   │   │   ├── address.controller.ts
│   │   │   ├── address.service.ts
│   │   │   ├── address.module.ts
│   │   │   └── 📁 dto/                # Data Transfer Objects
│   │   ├── 📁 auth/                   # Authentication & Authorization
│   │   │   ├── auth.controller.ts
│   │   │   ├── auth.service.ts
│   │   │   ├── auth.module.ts
│   │   │   ├── jwt.strategy.ts
│   │   │   ├── 📁 dto/                # Login, Register DTOs
│   │   │   └── 📁 guards/             # JWT, Admin, Roles guards
│   │   ├── 📁 common/                 # Shared services & utilities
│   │   │   ├── common.module.ts
│   │   │   ├── 📁 controllers/        # Geocoding, Analytics controllers
│   │   │   ├── 📁 decorators/         # Custom decorators (User, Roles)
│   │   │   ├── 📁 filters/            # Exception filters
│   │   │   ├── 📁 gateways/           # WebSocket gateway for real-time
│   │   │   ├── 📁 guards/             # Common guards
│   │   │   ├── 📁 pipes/              # Validation pipes
│   │   │   └── 📁 services/           # Email, Geocoding, Pricing services
│   │   ├── 📁 config/                 # Configuration files
│   │   │   ├── app.config.ts
│   │   │   ├── jwt.config.ts
│   │   │   └── mail.config.ts
│   │   ├── 📁 courier/                # Courier management module
│   │   │   ├── courier.controller.ts
│   │   │   ├── courier.service.ts
│   │   │   ├── courier.module.ts
│   │   │   ├── 📁 dto/                # Courier DTOs
│   │   │   └── 📁 entities/           # Courier entities
│   │   ├── 📁 notification/           # Notification system
│   │   │   ├── notification.controller.ts
│   │   │   ├── notification.service.ts
│   │   │   ├── notification.module.ts
│   │   │   └── 📁 dto/                # Notification DTOs
│   │   ├── 📁 parcel/                 # Parcel management module
│   │   │   ├── parcel.controller.ts
│   │   │   ├── parcel.service.ts
│   │   │   ├── parcel.module.ts
│   │   │   ├── public-tracking.controller.ts
│   │   │   ├── 📁 dto/                # Parcel DTOs
│   │   │   └── 📁 entities/           # Parcel entities
│   │   ├── 📁 prisma/                 # Database service
│   │   │   ├── prisma.module.ts
│   │   │   └── prisma.service.ts
│   │   ├── 📁 user/                   # User management module
│   │   │   ├── user.controller.ts
│   │   │   ├── user.service.ts
│   │   │   ├── user.module.ts
│   │   │   ├── 📁 dto/                # User DTOs
│   │   │   └── 📁 entities/           # User entities
│   │   ├── app.controller.ts          # Main app controller
│   │   ├── app.service.ts             # Main app service
│   │   ├── app.module.ts              # Root application module
│   │   └── main.ts                    # Application entry point
│   ├── 📁 prisma/                     # Database schema & migrations
│   │   ├── schema.prisma              # Database schema definition
│   │   └── 📁 migrations/             # Database migration files
│   ├── 📁 test/                       # Test files
│   ├── 📁 dist/                       # Compiled JavaScript output
│   ├── 📁 generated/                  # Generated Prisma client
│   ├── 📁 restclient/                 # REST client test files
│   ├── package.json                   # Backend dependencies
│   ├── tsconfig.json                  # TypeScript configuration
│   ├── nest-cli.json                  # NestJS CLI configuration
│   ├── eslint.config.mjs              # ESLint configuration
│   ├── render.yaml                    # Render deployment config
│   └── seed-data.js                   # Database seeding script
│
├── 📁 sendit-frontend/                # Angular Frontend Application
│   ├── 📁 src/
│   │   ├── 📁 app/
│   │   │   ├── 📁 admin/              # Admin dashboard module
│   │   │   │   ├── 📁 admin-dashboard/
│   │   │   │   ├── 📁 analytics/
│   │   │   │   ├── admin-module.ts
│   │   │   │   └── admin-routing-module.ts
│   │   │   ├── 📁 auth/               # Authentication module
│   │   │   │   ├── 📁 login/          # Login component
│   │   │   │   ├── 📁 register/       # Registration component
│   │   │   │   ├── auth-module.ts
│   │   │   │   └── auth-routing-module.ts
│   │   │   ├── 📁 core/               # Core services & guards
│   │   │   │   ├── 📁 guards/         # Auth guards
│   │   │   │   ├── 📁 interceptors/   # HTTP interceptors
│   │   │   │   └── 📁 services/       # Core services
│   │   │   ├── 📁 courier/            # Courier dashboard module
│   │   │   │   ├── 📁 courier-dashboard/
│   │   │   │   ├── courier-module.ts
│   │   │   │   └── courier-routing-module.ts
│   │   │   ├── 📁 shared/             # Shared components
│   │   │   │   ├── 📁 components/     # Reusable components
│   │   │   │   │   ├── 📁 map/        # Google Maps component
│   │   │   │   │   ├── 📁 header/     # Header component
│   │   │   │   │   └── 📁 footer/     # Footer component
│   │   │   │   └── 📁 services/       # Shared services
│   │   │   ├── 📁 user/               # User dashboard module
│   │   │   │   ├── 📁 dashboard/      # User dashboard
│   │   │   │   ├── 📁 send-parcel/    # Send parcel form
│   │   │   │   ├── 📁 track-parcel/   # Parcel tracking
│   │   │   │   ├── 📁 notification-center/ # Notifications
│   │   │   │   ├── user-module.ts
│   │   │   │   └── user-routing-module.ts
│   │   │   ├── app.ts                 # Root component
│   │   │   ├── app.html               # Root template
│   │   │   ├── app.css                # Root styles
│   │   │   ├── app-module.ts          # Root module
│   │   │   ├── app-routing-module.ts  # Main routing
│   │   │   ├── core-module.ts         # Core module
│   │   │   ├── landing.ts             # Landing page component
│   │   │   └── landing.html           # Landing page template
│   │   ├── 📁 assets/                 # Static assets
│   │   │   └── 📁 images/             # Images and icons
│   │   ├── 📁 environments/           # Environment configurations
│   │   │   ├── environment.ts         # Development environment
│   │   │   └── environment.prod.ts    # Production environment
│   │   ├── index.html                 # Main HTML file
│   │   ├── main.ts                    # Application bootstrap
│   │   └── styles.css                 # Global styles
│   ├── 📁 dist/                       # Built application
│   ├── 📁 public/                     # Public assets
│   ├── package.json                   # Frontend dependencies
│   ├── angular.json                   # Angular CLI configuration
│   ├── tsconfig.json                  # TypeScript configuration
│   ├── tsconfig.app.json              # App-specific TypeScript config
│   ├── tsconfig.spec.json             # Test TypeScript config
│   └── vercel.json                    # Vercel deployment config
│
├── 📁 src/                            # Legacy/Additional source files
│   └── 📁 app/
│       └── 📁 core/
│           └── 📁 guards/
│               └── auth-guard.ts      # Shared auth guard
│
├── 📁 template/                       # HTML templates & mockups
│   ├── landing_page.html
│   ├── send_parcel.html
│   ├── sendit_courier_dashboard.html
│   ├── sendit_dashboard_admin.html
│   ├── sendit_dashboard.html
│   ├── sendit_login_page.html
│   ├── sendit_notification_center.html
│   ├── sendit_signup.html
│   └── sendit_tracking.html
│
├── 📄 README.md                       # Project documentation (this file)
├── 📄 DEPLOYMENT.md                   # Deployment guide
├── 📄 GOOGLE_MAPS_INTEGRATION.md      # Google Maps integration docs
├── 📄 flow.txt                        # Application flow documentation
├── 📄 progress.txt                    # Development progress notes
├── 📄 template_folder.md              # Template documentation
├── 📄 package.json                    # Root package.json
├── 📄 package-lock.json               # Root package lock
└── 📁 node_modules/                   # Root dependencies
```

### **Key Directory Explanations**

#### **Backend Structure (`sendit-backend/`)**

- **`src/`** - Main source code directory
- **`auth/`** - JWT authentication, login/register, guards
- **`common/`** - Shared services (email, geocoding, pricing, WebSocket)
- **`parcel/`** - Core parcel management functionality
- **`user/`** - User management and profiles
- **`courier/`** - Courier-specific functionality
- **`notification/`** - Multi-channel notification system
- **`prisma/`** - Database schema and migrations

#### **Frontend Structure (`sendit-frontend/`)**

- **`src/app/`** - Main application code
- **`admin/`** - Admin dashboard and management tools
- **`auth/`** - Login/register components
- **`user/`** - User dashboard, send/track parcels
- **`courier/`** - Courier dashboard and delivery management
- **`shared/`** - Reusable components (map, header, footer)
- **`core/`** - Services, guards, interceptors

#### **Configuration Files**

- **`package.json`** - Dependencies and scripts
- **`tsconfig.json`** - TypeScript compilation settings
- **`angular.json`** - Angular CLI configuration
- **`prisma/schema.prisma`** - Database schema definition
- **`.env`** - Environment variables (not in repo)

#### **Documentation**

- **`README.md`** - This comprehensive documentation
- **`DEPLOYMENT.md`** - Production deployment guide
- **`GOOGLE_MAPS_INTEGRATION.md`** - Maps integration details
- **`flow.txt`** - Application workflow documentation

---

## 🙏 Acknowledgments

- **Angular Team** - For the amazing frontend framework
- **NestJS Team** - For the powerful backend framework
- **Prisma Team** - For the excellent database toolkit
- **Google Maps Platform** - For reliable mapping services
- **Vercel & Render** - For seamless deployment platforms
- **Open Source Community** - For the countless libraries and tools

---

## 📞 Support & Contact

- **GitHub Issues**: [Report bugs or request features](https://github.com/Maxmillian-Muiruri/Send-IT/issues)
- **Email**: [maxmillianmuiruri@gmail.com](mailto:maxmillianmuiruri@gmail.com)
- **LinkedIn**: [Maxmillian Muiruri](https://linkedin.com/in/maxmillian-muiruri)

---

<div align="center">

**Made with ❤️ by [Maxmillian Muiruri](https://github.com/Maxmillian-Muiruri)**

⭐ **Star this repository if you found it helpful!** ⭐

</div>
