# Expo Web Browser Doesn't Close on Android After Navigation

This repository demonstrates a bug where the Expo Web Browser on Android fails to close after navigating away from the opened URL. The issue occurs when using `expo-web-browser`'s `openBrowserAsync` method.

## Bug Description

The `openBrowserAsync` function opens the specified URL in a new browser tab or window. However, on Android devices, when the user navigates back to the app, the browser instance remains open in the background, consuming system resources. This doesn't happen on iOS.

## Reproduction Steps

1. Run the app on an Android emulator or device.
2. Tap the button to open the example URL.
3. Navigate away from the opened URL (e.g., by pressing the back button on the browser).
4. Observe that the browser remains open in the background. You might need to check your running apps or background processes.

## Workaround

Unfortunately, there's no direct fix for this currently within the `expo-web-browser` library. A possible workaround involves using an external library or implementing custom browser handling for Android.