# GUNI Login & Registration Android App

A beginner-friendly Android application that recreates the GUNI Login and Registration screens using Kotlin and Jetpack Compose.

## Features

- Login screen with email and password fields
- Registration screen with name, phone number, city, email, password, and confirm-password fields
- Navigation between Login and Registration screens
- Basic form validation
- Password visibility protection (password characters are hidden)
- GUNI logo displayed on both screens
- Responsive, scrollable registration form
- No Firebase, database, or backend API required

## Technology Stack

- **IDE:** Android Studio
- **Language:** Kotlin
- **UI:** Jetpack Compose
- **Design components:** Material 3
- **Navigation:** Navigation Compose
- **Minimum Android version:** API 23 or the minimum SDK configured in the project

## Project Structure

```text
app/
└── src/
    └── main/
        ├── java/com/example/a24012011153_mad_pr5/
        │   ├── MainActivity.kt
        │   ├── AppNavigation.kt
        │   ├── screen/
        │   │   ├── LoginPage.kt
        │   │   └── RegisterPage.kt
        │   └── ui/theme/
        │       ├── Color.kt
        │       ├── Theme.kt
        │       └── Type.kt
        ├── res/
        │   ├── drawable/
        │   │   └── guni_pink_logo.png
        │   └── values/
        └── AndroidManifest.xml
```

> Keep the package name consistent with your actual Android Studio project. If your project uses a different package name, update the package declarations and imports accordingly.

## Important: Add the GUNI Logo

The GUNI logo is supplied manually by the project owner.

1. Prepare the logo image in PNG format.
2. Copy it into:

   `app/src/main/res/drawable/guni_pink_logo.png`

3. Reference it in Compose code with:

   ```kotlin
   painterResource(id = R.drawable.guni_pink_logo)
   ```

Do not include the `.png` extension in the `R.drawable` resource name. Make sure the filename uses lowercase letters and underscores.

## Getting Started

1. Install and open Android Studio.
2. Open the project folder.
3. Wait for Gradle sync to finish.
4. Confirm that the required Jetpack Compose and Navigation Compose dependencies are present in the app-level `build.gradle.kts`.
5. Add the GUNI logo to the `res/drawable` folder.
6. Select an Android emulator or connect a phone with USB debugging enabled.
7. Click **Run ▶**.

## Screen Navigation

```text
Login Screen
    |
    | Tap SIGN UP
    v
Registration Screen
    |
    | Tap LOGIN
    v
Login Screen
```

## Validation

The app is intended to provide basic client-side checks:

- Login: check that email and password are entered.
- Registration: check required fields, email format, and whether password and confirm-password match.
- Show a message when validation fails or registration is completed.

This is a demonstration project only. Registration success does not create a real account unless a backend or persistent storage feature is added. Login does not authenticate a real user.

## Design

- Light background
- GUNI logo centered above the form
- Rounded lavender form card
- Purple Login button
- Blue Register button
- Grey outlined text fields
- Navigation links beneath each form

The goal is to match the supplied GUNI Login and Registration reference image while keeping the implementation simple.

## Troubleshooting

### `Unresolved reference: guni_pink_logo`
- Confirm the file exists at `app/src/main/res/drawable/guni_pink_logo.png`.
- Check the spelling and use `R.drawable.guni_pink_logo`.
- Sync or rebuild the project.

### `Unresolved reference: navigation`
- Ensure the Navigation Compose dependency is included in the app-level Gradle file.
- Sync the project.

### Package errors
- Check that every Kotlin file uses the package matching the folder and application code.
- Update imports if your package name differs.

### App does not build
- Read the first error shown in Android Studio's Build output.
- Confirm all referenced composable functions and dependencies exist.
- Re-sync Gradle and rebuild.

## Limitations

- No backend authentication
- No database or account storage
- No password recovery service
- No network connection required for the app's basic UI

## License

This project is intended for educational and university practical use. Add a license if you plan to distribute it publicly.
