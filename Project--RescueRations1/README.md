# RescueRations 🌍🍽️
> **Plate to Purpose: Rescue Food, Save Earth.**

RescueRations is a real-time web application connecting local restaurants with surplus food to consumers looking for affordable meals. By facilitating these "rescues," we help reduce food waste and lower CO2 emissions.

## ✨ Features

### 🏢 For Restaurants
-   **Real-time Listings:** Instantly post surplus food items.
-   **Inventory Management:** Track active listings and quantities.
-   **AI Surplus Prediction:** (Simulation) Tool to estimate surplus inventory.
-   **Impact Tracking:** Contribute to sustainability goals.

### 👤 For Consumers
-   **Live Feed:** View available food nearby in real-time.
-   **Interactive Map:** See pickup locations on a map (Google Maps integration).
-   **One-Click Rescue:** Seamless reservation and checkout process.
-   **Order History:** Track your past rescues and status.

### 🔐 Security & Tech
-   **Role-Based Access Control (RBAC):** Strict separation between Consumer and Restaurant views.
-   **Firebase Authentication:** Secure email/password login.
-   **Firestore Database:** Real-time data syncing for listings and orders.
-   **Atomic Transactions:** Prevents overselling of inventory.
-   **Responsive Design:** Works on Mobile and Desktop (Bootstrap 5).

## 🚀 Setup & Installation

### Prerequisites
-   A Google Firebase Account.
-   A Google Maps API Key.

### 1. Configuration
Ensure you have updated the configuration in `RescueRations.html`:
-   **Firebase Config:** Replace the placeholder object with your project keys.
-   **Google Maps API:** Replace the `key` parameter in the script tag.

*(See `FINAL_SETUP.md` for detailed step-by-step instructions).*

### 2. Local Usage
Simply open `RescueRations.html` in your web browser! No build process required.

## 📦 Deployment (Firebase Hosting)

This project is ready for Firebase Hosting.

1.  **Install Firebase CLI:**
    ```bash
    npm install -g firebase-tools
    ```

2.  **Login:**
    ```bash
    firebase login
    ```

3.  **Initialize (if not done):**
    ```bash
    firebase init hosting
    ```
    *Select "Use existing project" and choose your project `gdg-rbu-hack`.*

4.  **Deploy:**
    ```bash
    firebase deploy --only hosting
    ```

The `firebase.json` file included in this project handles the configuration, serving `RescueRations.html` as the default homepage.

## 🛠️ Technology Stack
-   **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
-   **Framework:** Bootstrap 5
-   **Backend:** Firebase (Firestore, Auth, Analytics)
-   **API:** Google Maps JavaScript API
-   **Libraries:** Canvas Confetti

## 📄 License
This project is open-source and available for educational and hackathon purposes.
