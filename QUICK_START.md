# MoodQuest - Quick Start Guide

## 🎉 Welcome to MoodQuest!

Your mood-based adventure planner is ready to help you discover spontaneous activities!

## 📱 What You Just Built

A fully functional Android app with:
- ✅ **Mood-based activity recommendations** (36 pre-loaded activities)
- ✅ **Custom activity creation** 
- ✅ **Location-aware filtering**
- ✅ **Adventure history tracking**
- ✅ **Material 3 design** with beautiful gradients
- ✅ **Room database** for offline persistence
- ✅ **Complete navigation** with bottom nav bar
- ✅ **Unit & instrumented tests**

## 🚀 How to Run

### Option 1: Open in Android Studio
1. Open Android Studio
2. Click "Open an Existing Project"
3. Navigate to `/Users/ndmx0/DEV/MoodQuest`
4. Wait for Gradle sync to complete
5. Click the green "Run" button or press `Ctrl+R`

### Option 2: Command Line
```bash
cd /Users/ndmx0/DEV/MoodQuest
./gradlew installDebug
```

## 🎯 First Time Setup

### 1. Sync Gradle
When you first open the project, Android Studio will automatically sync Gradle dependencies. This may take a few minutes.

### 2. Configure SDK
Ensure you have:
- Android SDK 36 installed
- Build Tools 34.0.0+
- JDK 17

### 3. Run on Emulator or Device
- **Emulator**: Use Android Studio AVD Manager to create a device (API 26+)
- **Physical Device**: Enable Developer Options and USB Debugging

## 🧪 Testing Your App

### Run Unit Tests
```bash
./gradlew test
```

### Run Instrumented Tests
```bash
./gradlew connectedAndroidTest
```

### Test Coverage
- ✅ Mood category mapping
- ✅ Location type enums
- ✅ Room database operations
- ✅ Activity queries and filtering

## 🎨 App Features to Try

### Home Screen
1. **Adjust the mood slider** - Watch the emoji and color change!
2. **Tap "Plan Adventure!"** - Get a random activity suggestion
3. **Enable location** - See the location toggle appear
4. **Add custom activity** - Tap the + button

### History Screen
1. Navigate using bottom nav bar
2. View your adventure history
3. Delete entries with the trash icon

### Settings Screen
1. Adjust location search radius (1-50 km)
2. Change theme preferences
3. View app version and about info

## 🔧 Troubleshooting

### Gradle Sync Issues
- Ensure internet connection for dependency downloads
- Try: File → Invalidate Caches → Restart

### Build Errors
- Clean build: Build → Clean Project
- Rebuild: Build → Rebuild Project

### Emulator Issues
- Ensure virtualization is enabled in BIOS
- Allocate sufficient RAM (2GB minimum)

### Permission Issues
- Location permissions are optional
- App works fully without location access
- Grant permissions when prompted for nearby suggestions

## 📝 Key Files to Explore

### Core Logic
- `MainActivity.kt` - App entry point
- `AdventureViewModel.kt` - Business logic
- `AppDatabase.kt` - Room database setup
- `SeedData.kt` - 36 pre-populated activities

### UI Components
- `HomeScreen.kt` - Main interface
- `MoodSlider.kt` - Custom gradient slider
- `AdventureCard.kt` - Activity display
- `NavGraph.kt` - Navigation setup

### Data Layer
- `Activity.kt` - Activity data model
- `ActivityDao.kt` - Database queries
- `ActivityRepository.kt` - Data abstraction

## 🎨 Customization Ideas

### Add More Activities
Edit `SeedData.kt` to add more pre-populated activities.

### Change Colors
Edit `Color.kt` to customize the theme colors.

### Modify Mood Categories
Adjust mood thresholds in `AdventureViewModel.kt`:
- Currently: 0-25 (Relaxed), 26-50 (Creative), 51-75 (Adventurous), 76-100 (Energetic)

### Add New Features
- Weather API integration
- Photo uploads
- Social sharing
- Streak tracking
- Achievement system

## 📚 Architecture Overview

```
┌─────────────────┐
│  MainActivity   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Navigation     │
│  (NavGraph)     │
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼         ▼
┌────────┐┌────────┐┌──────────┐
│  Home  ││History ││ Settings │
└───┬────┘└───┬────┘└──────────┘
    │         │
    └────┬────┘
         ▼
┌─────────────────┐
│  ViewModel      │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│  Repository     │
└────────┬────────┘
         │
    ┌────┴────┐
    ▼         ▼
┌────────┐┌────────┐
│  Room  ││Location│
│   DB   ││Manager │
└────────┘└────────┘
```

## 🚀 Next Steps

1. **Run the app** and test all features
2. **Add your own activities** to personalize it
3. **Explore the code** to understand the architecture
4. **Extend functionality** with the enhancement ideas
5. **Share with friends** and get feedback!

## 💡 Pro Tips

- The app uses MVVM architecture for clean separation of concerns
- All data persists locally - no internet required after first run
- Location permissions are handled gracefully with fallbacks
- Material 3 provides automatic dark mode support
- The mood slider uses gradient colors that match the mood category

## 🆘 Need Help?

Check out the detailed README.md for more information or review the inline code comments for implementation details.

Happy adventuring! 🗺️✨

