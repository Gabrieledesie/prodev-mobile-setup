# Task 1: Create Your First Mobile App

## Objective
Set up the first mobile application using Expo Router template and document the scaffolding process.

## Date
January 11, 2026

## Steps Followed

### 1. Project Setup
**Command:**
```bash
cd prodev-mobile-setup
mkdir prodev-mobile-app-0x00
cd prodev-mobile-app-0x00
npx create-expo-app@latest app-example --template tabs
```

**What Happened:**
- Created new directory `prodev-mobile-app-0x00`
- Initialized Expo project with Router template using tabs
- Installed all dependencies automatically
- Created file structure with tabs navigation
- Template version: Expo SDK 54

### 2. Modified Home Screen
**File Modified:** `app-example/app/(tabs)/index.tsx`

**Changes Made:**
- Located the title text: "Tab One"
- Changed to: "First App Created"

**Code Change:**
```typescript
// Before:
<Text style={styles.title}>Tab One</Text>

// After:
<Text style={styles.title}>First App Created</Text>
```

### 3. Running the Application
**Command:**
```bash
cd app-example
npx expo start
```

**Testing Results:**
- Started Metro Bundler successfully
- QR code generated in terminal
- Opened application in web browser at localhost:8081
- Application loaded successfully
- Verified "First App Created" text displays correctly in the center of the screen

**Available Scripts:**
- `npm run start` - Start Expo development server
- `npm run android` - Start on Android device/emulator
- `npm run ios` - Start on iOS device/simulator
- `npm run web` - Start in web browser

### 4. Reset Project Observation
**Command Attempted:**
```bash
npm run reset-project
```

**Observations:**
The `reset-project` script does not exist in the current Expo template (Expo SDK 54, January 2026).

**Finding:**
When checking available scripts with `npm run`, only the following scripts are available:
- start
- android
- ios
- web

**Conclusion:**
The `reset-project` command was likely part of older Expo templates but has been removed in recent versions. Modern Expo templates come with a cleaner starting point and don't require a reset command. This change suggests that:
- Newer templates are already minimal and production-ready
- The boilerplate code is now considered useful rather than excessive
- Developers can start building immediately without needing to "reset" the project

**Alternative Approach:**
If you want a completely clean slate, you would:
1. Manually delete unwanted files and components
2. Or start with a blank template: `npx create-expo-app@latest --template blank`

### 5. Project Structure
```
prodev-mobile-app-0x00/
├── README.md (this file)
└── app-example/
    ├── app/
    │   ├── (tabs)/
    │   │   ├── index.tsx (modified - shows "First App Created")
    │   │   ├── explore.tsx
    │   │   └── _layout.tsx
    │   ├── _layout.tsx
    │   └── +not-found.tsx
    ├── constants/
    │   └── Colors.tsx
    ├── components/
    │   ├── Themed.tsx
    │   ├── EditScreenInfo.tsx
    │   └── navigation/
    ├── assets/
    ├── package.json
    └── node_modules/
```

## Environment Details
- **Node.js Version:** v22.16.0
- **npm Version:** 10.9.2
- **Expo SDK:** 54.0.31
- **Template:** tabs (Expo Router with tabs navigation)
- **Device Testing:** Web browser (localhost:8081)
- **Operating System:** Windows

## Key Files Modified
1. **app/(tabs)/index.tsx** - Home screen with modified title text "First App Created"

## Key Files (Unchanged)
2. **constants/Colors.tsx** - Theme color definitions for light/dark mode

## Challenges Faced

**Challenge 1:** Understanding the new Expo Router file structure
- **Solution:** Reviewed the generated files and Expo Router documentation

**Challenge 2:** Locating the text to modify (no "Welcome!" text found)
- **Solution:** Found "Tab One" text in the title and changed it to "First App Created"

**Challenge 3:** `reset-project` script not available
- **Solution:** Documented that this script has been removed in newer Expo templates

**Challenge 4:** Running commands from wrong directory
- **Solution:** Ensured all npm commands are run from the `app-example` directory where package.json exists

## What I Learned
1. Expo Router uses a file-based routing system where files in `app/` directory become routes
2. The `(tabs)` folder creates a tab-based navigation layout
3. Modern Expo templates are cleaner and don't require a reset command
4. Metro Bundler handles hot reloading automatically
5. The same app can run on web, iOS, and Android from a single codebase

## Next Steps
- Test the app on a physical Android device using Expo Go
- Explore the second tab (explore.tsx)
- Customize theme colors in Colors.tsx
- Add new screens and navigation routes
- Build more complex React Native components

---
*Task completed on: January 11, 2026*
