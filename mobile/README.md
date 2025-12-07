# Masked Face Recognition App

A Flutter application for recognizing faces, optimized for masked faces using eye-region features. This app connects to a Python backend (served via Hugging Face Spaces or Docker).

## Features
- **Real-time Recognition**: Capture or upload photos to recognize faces.
- **Mask Robust**: Specifically designed to work well even when the subject is wearing a mask.
- **Fast**: Optimized for quick response times.

## Getting Started

### Prerequisites
- Flutter SDK installed.
- The backend server running (see backend README).

### Configuration
1. Open `lib/core/config.dart`.
2. Update the `BASE_URL` with your backend URL.
   ```dart
   static const String BASE_URL = 'https://YOUR-SPACE-NAME.hf.space';
   ```
   *Note: If running locally with Docker, use your local IP address (e.g., `http://192.168.1.5:7860`).*

### Running the App
```bash
# Get dependencies
flutter pub get

# Run on connected device
flutter run
```

## structure
- `lib/core`: Configuration and constants.
- `lib/screens`: UI screens (Home, Recognition, etc.).
- `lib/services`: API handling.
- `lib/widgets`: Reusable UI components.
