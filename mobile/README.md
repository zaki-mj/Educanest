# Educanest Mobile Application

> **Cross-Platform Mobile Client for Parents & Educators**  
> Developed as part of the **Educanest** Kindergarten Management Platform  
> **École Supérieure en Informatique de Sidi-Bel-Abbès (ESI-SBA)**

---

## About the Mobile App

The **Educanest Mobile Application** is built with [Flutter](https://flutter.dev/) to offer parents and teachers an intuitive, responsive, and seamless experience on both Android and iOS devices. 

It eliminates traditional paper notebooks and fragmented group chats by providing dedicated role-based portals for classroom management, student tracking, meal schedules, and private in-app communication.

---

## Core Features

### 1. Authentication & Role Selection
* **Role-Based Onboarding**: Users select whether they are logging in as a **Teacher** or **Parent**.
* **Secure Registration**: Sign-up workflow requiring full name, email, password, and institution **School Code**.
* **Email Verification**: Two-step email verification via one-time confirmation codes.
* **Account Recovery**: Self-service password reset and recovery via email verification.

---

### 2. Teacher Experience
* **Teacher Dashboard**: Fast navigation across assigned classes and sections.
* **Weekly Timetables**: Visual weekly activity schedules outlining subjects, snack breaks, nap times, and outdoor play.
* **Student Roster**: Interactive search and directory of all students enrolled in the teacher's classes.
* **Subject Notes & Grading**: Enter and update performance in core areas (e.g., Mathematics, Arabic, French, English, Islamic Studies).
* **Behavioral & Developmental Remarks**: Expandable evaluation categories for holistic child development:
  * Psychology & Emotions
  * Discipline & Independence
  * Social Skills & Teamwork
  * Confidence & Communication
  * Listening & Speaking
  * Imagination & Creativity

---

### 3. Parent Experience
* **Weekly Nutrition & Meal Plan**: View daily morning snacks, hot lunches, and afternoon treats planned by the kindergarten.
* **Child Profile & Portfolio**: View academic progress, teacher remarks, and developmental observations.
* **Multi-Child Switcher**: Easily toggle between siblings enrolled in the kindergarten from the home screen.
* **Class Schedule**: Direct access to the child's daily and weekly activity timetables.

---

### 4. In-App Messaging & Community
* **Direct Teacher-Parent Messaging**: Secure, professional communication channel that eliminates the need to share private phone numbers.
* **Teacher-to-Teacher Chat**: In-app collaboration between educators.
* **Administration Inquiries**: Quick communication line with the kindergarten administration.

---

### 5. Settings & Profile Management
* **Account Profile**: Edit personal details (name, email, phone number).
* **Security**: Update password with validation.
* **Preferences**: Notification toggles and language options.
* **Persistent Sessions**: JWT-based authentication stored securely in device storage.



---

## Dependencies

The application relies on key Flutter packages:

| Package | Version | Purpose |
| :--- | :--- | :--- |
| **`flutter`** | SDK | Core UI framework |
| **`http`** | `^1.3.0` | HTTP requests to backend REST API |
| **`shared_preferences`**| `^2.5.3` | Persistent local storage for JWT authentication tokens |
| **`jwt_decoder`** | `^2.0.1` | Decoding JWT payload client-side for user ID and role |
| **`flutter_lints`** | `^5.0.0` | Official Flutter lint rules and code conventions |

---

## Getting Started

### 1. Prerequisites
* [Flutter SDK](https://docs.flutter.dev/get-started/install) (`>=3.6.1`)
* Android Studio (with Android SDK & Emulator) or Xcode (for iOS Simulator)
* Running instance of the [Educanest Backend](../backend)

### 2. Configure Backend API URL
By default, `lib/services/api_service.dart` uses `http://10.0.2.2:5000` (the standard alias for Android emulators to access the host machine's localhost):

* **For Android Emulator**: Keep `http://10.0.2.2:5000`.
* **For iOS Simulator**: Change the host to `http://localhost:5000`.
* **For Physical Device**: Change the host to your machine's local IP address (e.g., `http://192.168.1.50:5000`).

### 3. Installation & Run
1. Open terminal inside the `mobile` directory:
   ```bash
   cd mobile
   ```

2. Download project dependencies:
   ```bash
   flutter pub get
   ```

3. Run the app in debug mode on your connected device or emulator:
   ```bash
   flutter run
   ```

### 4. Build for Release
* **Generate Android APK**:
  ```bash
  flutter build apk --release
  ```
* **Generate Android App Bundle (AAB)**:
  ```bash
  flutter build appbundle --release
  ```

---

## Related Documentation
* Academic Report: [MULTIDISCIPLINARY PROJECT REPORT.pdf](../MULTIDISCIPLINARY%20PROJECT%20REPORT.pdf)
