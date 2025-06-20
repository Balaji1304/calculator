# Heavy Vehicles Management & Billing System

A modern web application designed to streamline the management of heavy vehicle operations. This system provides comprehensive tools for managing drivers, trucks, and billing processes, with a secure authentication system and intuitive dashboard to enhance operational efficiency.

## Features

- **Landing Page:** 
  - Professional introduction and service highlights.
  - Integrated contact form for inquiries.
- **Authentication:** 
  - Secure login for authorized users using email/password via Firebase.
- **Dashboard:** 
  - Centralized overview of key metrics, including drivers, trucks, billing statuses, and maintenance alerts.
- **Drivers Management:** 
  - Add, edit, delete, and list drivers with detailed information such as license details, experience, and status.
- **Trucks Management:** 
  - Comprehensive management for your truck fleet including registration, insurance, maintenance logs, and status tracking.
- **Billing Management:** 
  - Create, update, delete, and mark client bills as paid.
  - Export billing details to PDF for record-keeping.
- **Responsive UI:** 
  - Clean and modern design powered by Tailwind CSS, ensuring that the application is fully responsive across devices.
- **Protected Routes:** 
  - Only authenticated users can access management and dashboard pages, ensuring data security.

## Screenshots

Screenshots of key pages can be found in the `project/screenshots` directory:
- **Landing Page:** `landing.png`
- **Login:** `login.png`
- **Dashboard:** `dashboard.png`
- **Drivers Management:** `drivers.png`
- **Trucks Management:** `trucks.png`
- **Billing Management:** `billing.png`

## Tech Stack

- **Frontend:** React, TypeScript, Vite
- **Styling:** Tailwind CSS
- **Routing:** React Router DOM
- **State Management:** React Context API
- **Backend/Database:** Firebase Firestore for data handling and Firebase Authentication for secure login
- **PDF Export:** react-to-pdf
- **Icons:** lucide-react

## Getting Started

### Prerequisites

- Node.js (v16+ recommended)
- npm or yarn

### Installation

1. **Clone the Repository:**
   ```bash
   git clone <your-repo-url>
   cd project
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Configure Firebase:**
   - Create a Firebase project by visiting the [Firebase Console](https://console.firebase.google.com/).
   - Enable Authentication (Email/Password) and Firestore Database.
   - Copy your Firebase configuration and paste it into `src/lib/firebase.ts`. If the file doesn't exist, create it using the template below:
     ```typescript
     // src/lib/firebase.ts
     import { initializeApp } from "firebase/app";
     import { getFirestore } from "firebase/firestore";
     import { getAuth } from "firebase/auth";

     const firebaseConfig = {
       apiKey: "YOUR_API_KEY",
       authDomain: "YOUR_AUTH_DOMAIN",
       projectId: "YOUR_PROJECT_ID",
       storageBucket: "YOUR_STORAGE_BUCKET",
       messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
       appId: "YOUR_APP_ID"
     };

     const app = initializeApp(firebaseConfig);
     export const db = getFirestore(app);
     export const auth = getAuth(app);
     ```

4. **Start the Development Server:**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Access the Application:**
   - Open your browser and visit [http://localhost:5173](http://localhost:5173) (or the port specified in your terminal).

## Project Structure

```
project/
├── src/
│   ├── components/      # Reusable UI components (forms, lists, navbar, etc.)
│   ├── contexts/        # React context for authentication
│   ├── lib/             # Firebase configuration
│   ├── pages/           # Main application pages (Dashboard, Drivers, Trucks, Billing, Login, Landing)
│   ├── App.tsx          # Main application and routing handler
│   └── main.tsx         # Application entry point
├── public/              # Static assets and public files
├── package.json         # Project metadata and scripts
├── tailwind.config.js   # Tailwind CSS configuration
└── ...                  # Other configuration and asset files
```

## Available Scripts

- `npm run dev` — Starts the development server.
- `npm run build` — Builds the project for production.
- `npm run preview` — Previews the production build.
- `npm run lint` — Lints the codebase.

## Customization

- **Styling:** Customize the look and feel by modifying Tailwind CSS classes or editing the Tailwind configuration.
- **Database:** Adjust Firestore collections and fields to suit your business logic.
- **Authentication:** Extend the authentication functionality with additional providers such as Google, if necessary.

## License

This project is licensed under the MIT License.
