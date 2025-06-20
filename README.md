```markdown
# Heavy Vehicles Management & Billing System

A modern web application designed to streamline the management of heavy vehicle operations. This project facilitates efficient handling of drivers, trucks, and billing processes through an intuitive and secure dashboard, leveraging modern web technologies.

## Features

- **Landing Page:** Professional introduction with service highlights and a contact form.
- **Authentication:** Secure login via Firebase (email/password based).
- **Dashboard:** Comprehensive overview of key statistics such as drivers, trucks, pending bills, and maintenance alerts.
- **Drivers Management:** Add, edit, delete, and view driver profiles with details like license, experience, and status.
- **Trucks Management:** Manage fleet information including registration, insurance, maintenance, and status.
- **Billing Management:** Create, update, delete, and mark bills as paid; export billing info to PDF.
- **Responsive Design:** Modern, responsive UI built with Tailwind CSS for optimal user experience.
- **Protected Routes:** Ensures only authenticated users can access sensitive areas.

## Tech Stack

- **Frontend:** React, TypeScript, Vite
- **Styling:** Tailwind CSS
- **Routing:** React Router DOM
- **State Management:** React Context API
- **Backend/Database:** Firebase Firestore (for data and authentication)
- **PDF Export:** react-to-pdf
- **Icons:** lucide-react

## Screenshots

Screenshots are available in the `screenshots` directory:
- Landing Page: `screenshots/landing.png`
- Login Page: `screenshots/login.png`
- Dashboard: `screenshots/dashboard.png`
- Drivers Management: `screenshots/drivers.png`
- Trucks Management: `screenshots/trucks.png`
- Billing Management: `screenshots/billing.png`

## Getting Started

### Prerequisites

- Node.js (v16+ preferred)
- npm or yarn

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd project
   ```

2. **Install dependencies:**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Configure Firebase:**
   - Create a Firebase project at [Firebase Console](https://console.firebase.google.com/).
   - Enable Authentication (Email/Password) and Firestore Database.
   - Copy your Firebase configuration and update `src/lib/firebase.ts` accordingly.

   Example `src/lib/firebase.ts`:
   ```typescript
   import { initializeApp } from "firebase/app";
   import { getFirestore } from "firebase/firestore";
   import { getAuth } from "firebase/auth";
   
   const firebaseConfig = {
     apiKey: "...",
     authDomain: "...",
     projectId: "...",
     storageBucket: "...",
     messagingSenderId: "...",
     appId: "..."
   };
   
   const app = initializeApp(firebaseConfig);
   export const db = getFirestore(app);
   export const auth = getAuth(app);
   ```

4. **Start the development server:**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

5. **Access the Application:**
   Open [http://localhost:5173](http://localhost:5173) in your browser.

## Project Structure

```
project/
├── src/
│   ├── components/      # Reusable UI components (forms, lists, navbar, etc.)
│   ├── contexts/        # React context for authentication
│   ├── lib/             # Firebase configuration and utilities
│   ├── pages/           # Main application pages (Dashboard, Drivers, Trucks, Billing, Login, Landing)
│   ├── App.tsx          # Main app and routing configuration
│   └── main.tsx         # Application entry point
├── public/              # Public assets and static resources
├── package.json         # Project metadata and dependencies
├── tailwind.config.js   # Tailwind CSS configuration
└── ...                  # Additional configuration files
```

## Available Scripts

- `npm run dev` — Launch the development server.
- `npm run build` — Build the application for production.
- `npm run preview` — Preview the production build locally.
- `npm run lint` — Run ESLint to analyze code quality.

## Customization

- **Styling:** Customize Tailwind CSS classes or configuration to match your design requirements.
- **Database:** Modify Firestore collections and fields to meet your specific business logic.
- **Authentication:** Extend support with additional providers (e.g., Google sign-in) via Firebase.

## License

This project is licensed under the MIT License.
```
