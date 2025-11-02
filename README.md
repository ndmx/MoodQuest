# MoodQuest

A mood-based adventure planner Android app that helps you discover spontaneous activities based on your current mood and location.

## Features

- **Mood-Based Suggestions**: Adjust a slider to match your current mood (Relaxed, Creative, Adventurous, or Energetic) and get personalized activity recommendations
- **Custom Activities**: Add your own activities to expand your adventure options
- **Location Awareness**: Optional location filtering to find nearby activities
- **Adventure History**: Track your completed adventures with timestamps
- **Material 3 Design**: Modern, beautiful UI with dynamic theming and smooth animations
- **Offline Support**: All data persists locally using Room database

## Tech Stack

- **Language**: Kotlin 2.0.21
- **UI Framework**: Jetpack Compose
- **Architecture**: MVVM with Repository pattern
- **Database**: Room for local persistence
- **Location**: Google Play Services Location API
- **Permissions**: Accompanist Permissions
- **Navigation**: Jetpack Compose Navigation
- **Material Design**: Material 3

## Project Structure

```
app/src/main/java/com/ndmx/moodquest/
├── data/
│   ├── model/          # Data classes (Activity, AdventureHistory)
│   ├── dao/            # Room DAO
│   ├── database/       # Room database and converters
│   └── repository/     # Repository pattern implementation
├── location/           # Location services wrapper
├── viewmodel/          # ViewModel with business logic
├── ui/
│   ├── screens/        # Screen composables (Home, History, Settings)
│   ├── components/     # Reusable UI components
│   ├── navigation/     # Navigation graph
│   └── theme/          # Material 3 theme, colors, typography
├── utils/              # Utility functions
└── MainActivity.kt     # Main entry point
```

## Requirements

- Android Studio Iguana or later
- Minimum SDK: 26 (Android 8.0)
- Target SDK: 36
- JDK 17

## Getting Started

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd MoodQuest
   ```

2. Open the project in Android Studio

3. Sync Gradle files

4. Run the app on an emulator or physical device

## How to Use

1. **Set Your Mood**: Use the slider on the home screen to adjust your current mood
2. **Plan Adventure**: Tap the "Plan Adventure!" button to get a random activity suggestion
3. **Add Custom Activities**: Tap the + button to add your own activities
4. **Enable Location** (Optional): Grant location permissions for nearby activity suggestions
5. **View History**: Navigate to the History tab to see your past adventures
6. **Adjust Settings**: Visit the Settings tab to customize location radius and theme

## Permissions

- **Location**: Optional - used to suggest nearby activities based on your current location

## Pre-populated Activities

The app comes with 36 diverse activities across four mood categories:
- **Relaxed**: Cafes, parks, meditation, bookstores
- **Creative**: Art galleries, workshops, photography walks
- **Adventurous**: New restaurants, hidden trails, escape rooms
- **Energetic**: Running, cycling, dancing, sports

## Testing

Run unit tests:
```bash
./gradlew test
```

Run instrumented tests:
```bash
./gradlew connectedAndroidTest
```

## Future Enhancements

- Weather API integration for indoor/outdoor suggestions
- Streak tracking and gamification
- Photo uploads for completed adventures
- Social sharing functionality
- ML Kit for mood pattern analysis
- Google Places API for real venue suggestions
- AR previews with ARCore

## License

This project is open source and available under the MIT License.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Author

Built with ❤️ for adventure seekers everywhere

