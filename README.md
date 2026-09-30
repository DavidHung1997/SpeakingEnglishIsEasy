# 🎙️ English Listening And Speaking

An Android application designed to help users improve their **English listening and speaking skills** through structured conversations and audio playback.

---


## ✨ Features

- 📚 **Subjects** — Browse learning topics organized by subject categories
- 📝 **Topics** — Each subject contains multiple conversation topics
- 🎧 **Audio Playback** — Listen to conversations with a built-in MP3 player (play, pause, seek, next/previous)
- ⬇️ **Download** — Download audio files for offline listening
- ❤️ **Favourites** — Mark favourite topics to revisit later
- 🔤 **Translate** — Quick access to translation for conversation content
- 📤 **Share** — Share the app with friends via any installed app
- ⭐ **Rate** — Rate the app directly on the Google Play Store
- 🔒 **Portrait Mode** — Optimized for portrait-only orientation

---

## 🏗️ Architecture

The app follows a simple **MVC-style** structure:

```
app/src/main/
├── assets/
│   └── SpeakingEnglishIsEasy.sqlite   # Pre-packaged SQLite database
├── java/com/example/admin/
│   ├── model/
│   │   ├── Subject.java               # Subject data model
│   │   ├── Topic.java                 # Topic data model (with MP3 link & download path)
│   │   └── Conversation.java          # Conversation data model
│   ├── adapter/
│   │   ├── SubjectAdapter.java        # ListView adapter for subjects
│   │   ├── TopicAdapter.java          # ListView adapter for topics
│   │   └── ConversationAdapter.java   # ListView adapter for conversations
│   └── speakingenglishiseasy/
│       ├── Subject_Activity.java      # Main screen — lists all subjects
│       ├── Topic_Activity.java        # Lists topics within a subject
│       └── Conversation_Activity.java # Shows conversation + audio player
└── res/
    ├── layout/                        # UI layout XML files
    ├── drawable/                      # Icons and drawables
    └── values/                        # Colors, strings, styles
```

### Data Flow
1. The SQLite database is bundled in `assets/` and copied to the device on first launch.
2. **Subject → Topic → Conversation** is the navigation hierarchy.
3. Audio is streamed or played from a downloaded local file via `MediaPlayer`.

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Language | Java |
| Platform | Android |
| Min SDK | API 15 (Android 4.0.3) |
| Target SDK | API 23 (Android 6.0) |
| Database | SQLite (bundled asset) |
| Audio | Android `MediaPlayer` |
| UI | `ListView`, `NavigationDrawer`, `Material Design` |
| Build | Gradle |

---

## 🚀 Getting Started

### Prerequisites

- [Android Studio](https://developer.android.com/studio) (any modern version)
- JDK 8 or higher
- An Android device or emulator (API 15+)

### Build & Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/DavidHung1997/SpeakingEnglishIsEasy.git
   cd SpeakingEnglishIsEasy
   ```

2. **Open in Android Studio**
   - File → Open → select the project folder

3. **Run the app**
   - Connect a device or start an emulator
   - Click ▶ **Run** or press `Shift+F10`

> The SQLite database is automatically copied from `assets/` to the device on first launch — no manual setup required.

---

## 📂 Project Structure

```
SpeakingEnglishIsEasy/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── assets/            # Bundled SQLite database
│   │   │   ├── java/              # Application source code
│   │   │   └── res/               # Layouts, drawables, values
│   │   ├── test/                  # Unit tests
│   │   └── androidTest/           # Instrumentation tests
│   └── build.gradle               # App-level build config
├── docs/                          # Project documentation
├── build.gradle                   # Project-level build config
├── gradle.properties
└── settings.gradle
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is open source. See the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**David Hung**
- GitHub: [@DavidHung1997](https://github.com/DavidHung1997)

---

> _Made with ❤️ to help learners improve their English listening and speaking._
