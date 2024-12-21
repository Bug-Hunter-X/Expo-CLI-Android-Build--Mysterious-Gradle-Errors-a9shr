# Expo CLI Android Build: Mysterious Gradle Errors

This repository demonstrates a scenario where the Expo CLI Android build process fails with an unclear Gradle error. The exact error message varies, but the underlying issue usually involves environment problems, dependency conflicts, or inconsistencies in the Android build configuration.  The solution focuses on troubleshooting techniques to identify the root cause.

## Bug Reproduction

The `expo_android_bug.js` file contains a simplified Expo project setup. Attempting to build this project using `expo build:android` may (or may not depending on your specific environment) result in an obscure Gradle error.

## Solution

The `expo_android_fix.js` file demonstrates the following troubleshooting steps:

1. **Clean the project:** Use `expo prebuild --clean` to remove any potentially corrupted build files.
2. **Check the Gradle version:** Ensure the Gradle version specified in your `android/build.gradle` file is compatible with Expo and your system.
3. **Verify dependencies:** Review the project dependencies in your `package.json` for any conflicts or outdated packages.
4. **Invalidate caches:** Invalidate caches and restart your IDE or system (this often helps with Android Studio).
5. **Check Android environment:** Verify Android SDK and NDK installations and ensure they are configured correctly (PATH environment variables).
6. **Examine the complete error log:** The full error message usually holds clues to the underlying problem. Look carefully for stack traces or other indications of the issue.
7. **Expo CLI Updates:** Ensure you're using the latest version of the Expo CLI (`npm update -g expo-cli`).