# ClaudeWatch

A WearOS companion app for Claude AI that delivers real-time notifications to your smartwatch whenever Claude requires input or completes tasks.

## Overview

ClaudeWatch seamlessly integrates with your Claude AI sessions, ensuring you never miss important updates or requests for input. Whether you're away from your desk or simply want instant notifications on your wrist, ClaudeWatch keeps you connected to your AI assistant.

## Features

- **Real-time Notifications**: Instant push notifications when Claude needs your input
- **Task Completion Alerts**: Get notified when Claude finishes executing tasks
- **Session Monitoring**: Track active Claude sessions directly from your watch
- **Quick Actions**: Respond to simple prompts directly from your wrist
- **Battery Efficient**: Optimized for minimal battery consumption on WearOS devices
- **Customizable Alerts**: Configure notification types and vibration patterns

## Requirements

- WearOS 3.0 or higher
- Android phone with Wear OS companion app
- Active Claude AI account
- Internet connectivity on both phone and watch

## Installation

1. Clone the repository:
```bash
git clone https://github.com/davidschreiber/claudewatch.git
```

2. Open the project in Android Studio

3. Build and install on your WearOS device:
```bash
./gradlew installDebug
```

## Configuration

1. Launch ClaudeWatch on your WearOS device
2. Follow the on-screen setup to pair with your Claude account
3. Grant necessary permissions for notifications
4. Customize notification preferences in Settings

## Architecture

The app consists of two main components:

- **Mobile App**: Handles Claude API integration and session monitoring
- **Wear App**: Displays notifications and provides quick actions on the watch

Communication between components uses the Wearable Data Layer API for reliable message passing.

## Development

### Prerequisites

- Android Studio Arctic Fox or later
- Android SDK 33+
- Kotlin 1.9+

### Building from Source

```bash
# Build both mobile and wear apps
./gradlew build

# Run tests
./gradlew test

# Generate release APK
./gradlew assembleRelease
```

### Project Structure

```
claudewatch/
├── mobile/          # Android phone companion app
├── wear/            # WearOS app
├── shared/          # Shared code and resources
└── gradle/          # Build configuration
```

## Privacy & Security

- All Claude session data is encrypted in transit
- No session content is stored on the watch
- Authentication tokens are securely stored in Android Keystore
- Minimal data collection - only what's necessary for functionality

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For issues, questions, or suggestions, please open an issue on GitHub.

## Acknowledgments

- Built with Jetpack Compose for Wear OS
- Uses Material3 design components
- Powered by Claude AI API

---

**Note**: This is an independent project and is not officially affiliated with Anthropic or Claude AI.