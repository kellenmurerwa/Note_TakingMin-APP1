# Note_TakingMin-APP
📝 Flutter Notes App with Firebase Integration. 

A fully functional note-taking application developed with Flutter, featuring user authentication and real-time data handling through Firebase, the app leverages the Provider package for structured and reactive state management.

Key Highlights:
Dedicated Auth Screens: Streamlined login and registration pages for a smooth user experience

Firebase Auth Integration: Secure email/password authentication with robust input checks

Firestore-Backed Notes: Create, modify, view, and delete notes in real time with Firestore

Provider Architecture: Reactive UI updates without relying on setState()

Live Sync with Firestore: Instant reflection of data changes across devices

Validated Forms: Strong form validation rules with helpful error messages

SnackBar Alerts: Visual feedback through color-coded messages

Modern UI: Clean, responsive interface built using Material Design 3 principles

Auto Login: Persistent login sessions after app restart

## Getting Started
This project serves as a foundation for building a note-taking Flutter app with Firebase backend services. Follow the steps below to get the project up and running.

📦 Prerequisites
Flutter SDK(https://docs.flutter.dev/get-started/install)

Android Studio or VS Code(https://docs.flutter.dev/get-started/editor)

A Firebase account (firebase.google.com)

🔧 Flutter Project Setup
Clone the repository:

git clone (https://github.com/kellenmurerwa/Note_TakingMin-APP1.git)
cd Note_TakingMin-APP1
Install dependencies:

flutter pub get

Run the app:
flutter run

🔥Firebase Setup Steps:

Create a Firebase Project

Go to Firebase Console(https://console.firebase.google.com/)

Click Add Project and follow the instructions.

Register the App

Click Add App (choose Android/iOS depending on your project)

Provide your app’s package name (found in android/app/build.gradle)

Download the google-services.json file (for Android) or GoogleService-Info.plist (for iOS)

Add google-services.json to Project

Place the file inside:
android/app/

Enable Firebase Authentication

In the Firebase Console, go to Authentication > Sign-in Method

Enable Email/Password

Set Up Firestore Database

Navigate to Firestore Database in the Firebase Console

Click Create Database, select Start in test mode, and choose your region

Generate Firebase Configuration

Run this in your terminal:

flutterfire configure

This will auto-generate firebase_options.dart used in your app

An Architecture Diagram:

lib/
├── models/
│   ├── app_user.dart         # Defines the user data structure
│   └── note.dart             # Represents a note with Firestore integration
├── provider/
│   ├── auth_provider.dart    # Manages authentication state
│   └── notes_provider.dart   # Handles notes state using real-time streams
├── repositories/
│   ├── auth_repository.dart  # Encapsulates Firebase Auth logic
│   └── notes_repository.dart # Manages Firestore CRUD operations
├── screens/
│   ├── sign_in_screen.dart   # UI for user sign-in
│   ├── sign_up_screen.dart   # UI for user registration
│   └── notes_screen.dart     # Main UI for displaying and managing notes
├── widgets/
│   ├── auth_wrapper.dart     # Redirects based on auth state
│   ├── add_note_dialog.dart  # Dialog for creating notes with input validation
│   └── edit_note_dialog.dart # Dialog for editing notes with input validation
├── utils/
│   └── validators.dart       # Common input validation functions
├── firebase_options.dart     # Auto-generated Firebase setup
└── main.dart                 # App entry point and provider initialization
