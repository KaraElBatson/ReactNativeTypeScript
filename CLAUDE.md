# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a React Native TypeScript project for a Turkish LGS/YKS Exam Prep Game. The project is designed to be a mobile-first, gamified study application that helps Turkish students prepare for national exams through adaptive practice, mock exams, and analytics. The project includes a comprehensive Product Requirements Document (PRD) in `prd.md` that details the complete vision and requirements.

## Development Commands

### Core Development Workflow
```bash
# Start Metro bundler (required for development)
npm start

# Run on Android
npm run android

# Run on iOS (requires pod installation first)
npm run ios

# Install iOS dependencies (first time only or after native deps update)
bundle install
bundle exec pod install
```

### Code Quality and Testing
```bash
# Run Jest tests
npm test

# Run single test file
npm test App.test.tsx

# Lint code
npm run lint

# TypeScript type checking (no explicit script - use IDE or VSCode)
```

### Native Build Commands
```bash
# Android specific commands
cd android && ./gradlew clean
cd android && ./gradlew build

# iOS specific commands
cd ios && xcodebuild -workspace ReactNativeTypeScript.xcworkspace -scheme ReactNativeTypeScript -configuration Debug build
```

## Project Architecture

### Technology Stack
- **Framework**: React Native 0.81.4 with TypeScript
- **JavaScript Runtime**: Hermes (default)
- **Build System**: Metro bundler for JavaScript, Gradle for Android, Xcode for iOS
- **Testing**: Jest with React Native preset
- **Linting**: ESLint with React Native configuration
- **Styling**: React Native StyleSheet (planned for Turkish UI patterns)

### Project Structure
```
ReactNativeTypeScript/
├── App.tsx                     # Main application component
├── prd.md                      # Product Requirements Document
├── __tests__/                  # Test files
│   └── App.test.tsx           # Basic app rendering test
├── android/                   # Android native project
│   ├── build.gradle           # Android project configuration
│   ├── settings.gradle        # Android module settings
│   └── app/                   # Android app module
├── ios/                       # iOS native project
│   ├── Podfile                # iOS dependencies configuration
│   └── ReactNativeTypeScript.xcodeproj/  # Xcode project
├── metro.config.js            # Metro bundler configuration
├── babel.config.js            # Babel transpilation configuration
├── tsconfig.json              # TypeScript configuration
├── jest.config.js             # Jest testing configuration
└── package.json               # Project dependencies and scripts
```

### Key Configuration Files

#### TypeScript Configuration
- Extends `@react-native/typescript-config`
- Includes all `.ts` and `.tsx` files
- Excludes `node_modules` and `Pods` directories

#### Metro Configuration
- Uses React Native's default Metro configuration
- Configurable for custom transformers or additional asset types

#### Babel Configuration
- Uses `@react-native/babel-preset`
- Supports React Native's JavaScript transformation requirements

#### Jest Configuration
- Uses React Native preset for React Native component testing
- Supports snapshot testing and component rendering tests

### Native Dependencies
- **iOS**: Uses CocoaPods for dependency management
- **Android**: Uses Gradle for dependency management
- Both platforms have their respective React Native native modules

## Development Guidelines

### TypeScript Usage
- All JavaScript/JSX files should use TypeScript (.ts/.tsx extensions)
- The project uses React Native's TypeScript configuration which includes proper typing for React Native APIs
- Type definitions are available through `@types/*` packages

### Component Structure
- Main app component is in `App.tsx` using React Native's `NewAppScreen` template
- Uses SafeAreaProvider for handling device safe areas
- Follows React Native's recommended component patterns

### Testing Approach
- Jest with React Native preset for component testing
- Test files should be placed in `__tests__` directory
- Basic test exists for app rendering verification

### Code Style
- ESLint configured with React Native rules
- Prettier configured for consistent code formatting
- TypeScript strict mode enabled through React Native's TS config

## Platform-Specific Considerations

### Android Development
- Gradle build system with standard React Native Android configuration
- Minimum SDK version defined in `android/build.gradle`
- Target SDK version follows React Native recommendations

### iOS Development
- Xcode project with CocoaPods dependency management
- iOS version requirements defined in Podfile
- Uses React Native's iOS template structure

## Future Development Notes

Based on the PRD, the project will need:
- Navigation setup (React Navigation)
- State management (likely Redux or Zustand)
- Database/Storage solutions (SQLite or AsyncStorage)
- Authentication system
- Payment integration
- Analytics tracking
- Custom UI components for Turkish exam preparation

The project is currently in early stages with the basic React Native template structure in place.