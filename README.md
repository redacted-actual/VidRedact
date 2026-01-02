VidRedact: AI Video Redactor for Android
VidRedact is a high-performance Android application designed to automate the process of redacting sensitive information from video files. By combining on-device computer vision with powerful video processing libraries, VidRedact allows users to blur or black out faces, text, and objects using simple natural language commands.
🚀 Features
AI-Assisted Detection: Automatically identifies faces, text, and logos using Google ML Kit.
NLP Command Interface: Specify redaction rules through text (e.g., "Blur all faces and license plates").
High-Fidelity Rendering: Powered by FFmpegKit to ensure original resolution and frame rates are maintained.
Privacy First: All processing is done locally on the device; no video data is ever uploaded to the cloud.
Progress Tracking: Real-time visual feedback during the analysis and rendering phases.
🛠️ Tech Stack
Language: Kotlin
AI Engines: Google ML Kit (Face Detection, Text Recognition, Object Detection)
Video Processing: FFmpegKit (Full LTS release)
Concurrency: Kotlin Coroutines
UI Architecture: MVVM with Material Design 3
📖 How It Works
Selection: The user selects a video file from the device storage.
Analysis: VidRedact scans the video at set intervals. The ML Kit vision models generate a map of coordinates (bounding boxes) for the specified targets.
Command Translation: The app converts these coordinates into a series of time-stamped FFmpeg filter instructions.
Rendering: FFmpeg applies a delogo or boxblur filter to the specific regions and re-encodes the video for export.
🏁 Getting Started
Prerequisites
Android Studio Iguana or newer.
Android SDK 26 (Oreo) or higher.
Device with an ARM64 processor (recommended for FFmpeg performance).
Installation
Clone the repository:
git clone https://github.com/yourusername/VidRedact.git
Open the project in Android Studio.
Sync Gradle and run the app on a physical device for optimal ML performance.

- Redacted 
