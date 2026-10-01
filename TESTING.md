# Urban Spoon — Testing & Credentials Guide

This document contains the credentials required to test various parts of the Urban Spoon application, including the Admin Dashboard and the Database.

## 🔐 Application Credentials

Use these credentials to log in to the Urban Spoon application.

| Role | Email | Password | Access Level |
| :--- | :--- | :--- | :--- |
| **Admin Portal** | `admin@urbanspoon.com` | `Admin@UrbanSpoon2026` | Full access to view and manage table reservations via the `/admin` dashboard. |
| **Customer Portal** | `kasimshah998@gmail.com` | `Kasim@2003` | Access to the user profile and ability to submit table reservations as a logged-in user. |

---

## 🧪 Comprehensive Testing Guide

Follow these steps to fully test the Urban Spoon application:

### 1. General UI & Navigation
- [ ] Navigate to the **Home page** and verify that all animations, hero images, and the navigation bar work properly.
- [ ] Verify that the navigation bar sticks to the top as you scroll.
- [ ] Check the footer links, social media icons, and address details.

### 2. Menu Section
- [ ] Go to the **Our Menu** page.
- [ ] Test the category filters (Starters, Main Course, Desserts, Beverages) to ensure dishes are filtered correctly.
- [ ] Use the search bar to search for specific dishes by name or ingredient.

### 3. Customer Authentication
- [ ] Click on the **Sign In** button in the navigation bar.
- [ ] Select the **Customer** tab.
- [ ] Log in using the Customer credentials (`kasimshah998@gmail.com`).
- [ ] Verify that the password field allows you to toggle visibility using the **Show/Hide** button.
- [ ] Verify successful login and check if the UI updates appropriately.

### 4. Table Reservation System
- [ ] Navigate to the **Contact** page or click the **Reserve a Table** button.
- [ ] Fill out the reservation form (Name, Phone, Date, Guests).
- [ ] Submit the form and verify that the confirmation success summary appears.
- [ ] Try submitting an empty form or invalid date to ensure validation errors are displayed.

### 5. Admin Dashboard (Real-time DB Verification)
- [ ] Sign out from the customer account (if logged in).
- [ ] Go to the **Sign In** page and select the **Administrator** tab.
- [ ] Log in using the Admin credentials (`admin@urbanspoon.com`).
- [ ] Once redirected to the `/admin` dashboard, verify that you can see all submitted table reservations.
- [ ] Check if the reservation you submitted in step 4 appears in the list.
- [ ] Use the search bar in the admin panel to search for specific names or dates.

### 6. Mobile Responsiveness
- [ ] Open the application on a mobile device or use browser developer tools to simulate a mobile screen.
- [ ] Verify that the hamburger menu works correctly.
- [ ] Ensure that grids (like the menu items and footer columns) stack neatly into a single column on smaller screens.
