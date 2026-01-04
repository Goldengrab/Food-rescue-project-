# RescueRations: Final Configuration Guide

Your application is now fully integrated with Firebase logic for Authentication, Firestore Database, and Real-time updates. However, to make it completely functional, you need to link it to your own Firebase Project.

## 1. Firebase Setup

### Step A: Create a Project
1. Go to [Firebase Console](https://console.firebase.google.com/).
2. Click **Add project** and follow the setup steps.
3. Enable **Google Analytics** if desired (optional).

### Step B: Enable Authentication
1. In your project dashboard, go to **Build > Authentication**.
2. Click **Get Started**.
3. Select **Email/Password** as a Sign-in provider and **Enable** it.

### Step C: Create Firestore Database
1. Go to **Build > Firestore Database**.
2. Click **Create Database**.
3. Choose a location (e.g., `asia-south1` for India or `us-central1`).
4. **Important**: Start in **Test mode** initially to verify connections, or switch to **Production mode** and paste the rules provided below.

### Step D: Get Configuration Keys
1. Go to **Project Settings** (Gear icon > Project settings).
2. Scroll down to **Your apps** and click the **Web (</>)** icon.
3. Register the app (nickname: "RescueRations").
4. Copy the `firebaseConfig` object (it looks like the code below).

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "...",
  projectId: "...",
  storageBucket: "...",
  messagingSenderId: "...",
  appId: "..."
};
```

### Step E: Update Code
1. Open `RescueRations.html`.
2. Locate the `firebaseConfig` section (around line 377).
3. **Replace** the placeholder values with your actual keys from Step D.

---

## 2. Security Rules

To protect your data and ensure only Restaurants can add food, use the provided Security Rules.

1. In Firebase Console, go to **Firestore Database > Rules**.
2. Copy the content of the `firestore.rules` file included in this project.
3. Paste it into the editor and click **Publish**.

---

## 3. Google Maps API

The application uses Google Maps to show locations.
1. Go to [Google Cloud Console](https://console.cloud.google.com/).
2. Create a Project and enable **Maps JavaScript API**.
3. Create an **API Key**.
4. In `RescueRations.html`, find the `<script>` tag for Maps (around line 369).
5. Replace `key=AIzaSyAlmOx18TXTwr6S7z0FmxrgB_dWyI3vZhg` with your own API Key.

---

## 4. Testing the App

1. Open `RescueRations.html` in your browser.
2. **Sign Up** as a **Restaurant** first.
   - Go to "Restaurant Login" -> "Sign Up".
   - You should be able to "Add New Listing".
3. **Sign Up** as a **Consumer** in a different browser/incognito window.
   - You should see the listings added by the restaurant.
   - Click "Rescue Now" to place an order.
   - Check "My Orders" (scroll down in Consumer Dashboard) to see your rescue!

Enjoy your fully agentic, real-time Food Rescue app! 🌍🍽️
