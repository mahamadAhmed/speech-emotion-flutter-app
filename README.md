# Speech Emotion Recognition Mobile Client (Flutter)

A cross-platform mobile client application for real-time speech emotion inference. Users can record voice clips, send audio payloads to a dedicated Flask inference server, and review classified affective states alongside historical analysis.

## Key Capabilities

- **Voice Acquisition:** Integrated in-app audio recording and waveform playback.
- **REST Inference Communication:** Transmits audio recordings as multipart payloads to the emotion classification API.
- **Affective State Display:** Presents predicted emotion categories (Happy, Sad, Angry, Neutral) with confidence estimates.
- **Historical Tracking:** Allows users to review and replay prior voice emotion evaluations.
- **User Authentication:** Sign-up, login, and profile management workflows supported via Firebase and backend services.

## Architecture

```mermaid
flowchart LR
    A[Mobile Client: Flutter UI] -->|Record Voice| B[Audio Buffer / WAV]
    B -->|Multipart HTTP POST| C[Inference Backend API]
    C -->|Extract Features & 1D CNN| D[Emotion Classification Engine]
    D -->|JSON Result| A
```

## Directory Structure

```text
├── lib/                      # Flutter client application
│   ├── main.dart             # Application initialization
│   ├── screens/              # Onboarding, authentication, and core dashboards
│   ├── page-1/               # Voice recording, audio player, and result views
│   └── Server/               # API endpoint configurations and data models
├── backend/                  # Dedicated backend services
│   └── php/                  # Authentication & database helper endpoints
├── assets/                   # Graphical assets and UI icons
├── pubspec.yaml              # Flutter package dependencies
└── README.md                 # Project documentation
```

## Setup & Running

1. Ensure Flutter SDK is installed and configured (`flutter doctor`).
2. Install dependencies:
   ```bash
   flutter pub get
   ```
3. Run the application on a connected device or emulator:
   ```bash
   flutter run
   ```

## Author

**Mahamat Ahmat**  
* M.Sc. Artificial Intelligence Engineering — University of Passau
* B.Sc. in Artificial Intelligence — Cairo University
* Portfolio: [mohamedgpt.me](https://mohamedgpt.me)
* GitHub: [@mahamadAhmed](https://github.com/mahamadAhmed)
