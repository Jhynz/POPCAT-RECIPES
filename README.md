PopCat Recipes Web App

Overview

PopCat Recipes is a mobile-first, single-page web application (SPA) designed for sharing and managing recipes. Built with a fun, "PopCat" meme-inspired aesthetic, it features a robust backend using Firebase for authentication and real-time data storage. Users can browse public recipes, manage their own private cookbook, and save their favorites.

Features

🔐 Authentication & User Management

Sign Up & Login: Secure email/password authentication via Firebase Auth.

Profile Management: Displays user avatars and recipe counts.

Session Persistence: Keeps users logged in across page reloads.

🍳 Recipe Management

Create Recipes: Detailed form including prep time, cook time, servings, ingredients, and step-by-step instructions.

Public vs. Private: Users can choose to publish recipes to the global feed or keep them in their private "My Recipes" collection.

Edit & Delete: Full CRUD (Create, Read, Update, Delete) capabilities for the user's own content.

Interactive Details: Recipe detail view features an interactive ingredient checklist for cooking tracking.

🧭 Discovery & Navigation

Global Feed: Browse recipes shared by the community.

Search & Sort: Real-time search by title, ingredient, or chef. Sort by Date, Title, or Prep Time.

Category Filters: Filter recipes by tags like Breakfast, Dinner, Vegan, etc.

Favorites: "Heart" recipes to save them to a personal favorites list.

🎨 UI/UX Design

Mobile-First Interface: Designed to look and feel like a native mobile app.

Responsive: Adapts to desktop views while maintaining the mobile form factor.

Animations: Smooth transitions, loading skeletons, and "PopCat" themed loading screens.

Toast Notifications: Custom non-intrusive alerts for user feedback.

Tech Stack

Frontend: HTML5, CSS3, JavaScript (ES6 Modules)

Styling: Tailwind CSS (via CDN), Google Fonts (Inter family)

Backend: Firebase (Authentication, Firestore Database)

Icons: Inline SVGs and Placehold.co for placeholder images.

Setup & Installation

Prerequisites

Since this application uses JavaScript ES Modules (<script type="module">), you cannot simply double-click the index.html file to run it. Browsers block module requests from the file:// protocol for security reasons.

Method 1: VS Code Live Server (Recommended)

Open the project folder in Visual Studio Code.

Install the Live Server extension.

Right-click index.html and select "Open with Live Server".

Method 2: Python Simple Server

If you have Python installed, open your terminal/command prompt in the project folder and run:

Python 3: python -m http.server 8000

Then navigate to http://localhost:8000 in your browser.

Method 3: Node.js http-server

Install the package globally: npm install -g http-server

Run the command: http-server

Navigate to the provided localhost URL.

Firebase Configuration

The application is currently set up with a specific Firebase configuration. To host this yourself or use your own database:

Go to the Firebase Console.

Create a new project.

Enable Authentication (Email/Password provider).

Enable Cloud Firestore (Create database).

Note: Ensure your Firestore Security Rules allow read/write access for authenticated users.

In index.html, locate the firebaseConfig object inside the <script type="module"> block.

Replace the values (apiKey, authDomain, projectId, etc.) with your own project's credentials.

Customization

Theme Colors: Modify the :root variables in the CSS <style> block to change the color scheme.

--popcat-bg: Background color

--popcat-accent: Primary button and highlight color

App Icon: Replace popcat_icon.png and popcat_full.png with your own logo assets.

License

This project is open-source and available for personal and educational use.
