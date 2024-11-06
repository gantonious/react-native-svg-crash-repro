# react-native-svg 15.8.0 crash reproduction

This repo contains the minimum reproduction steps to reproduce an Android crash in react-native-svg under the following environment:

```
react-native: v0.76.0
react-native-svg: v15.8.0
react-native-svg-transformer: v1.5.0
new arch: disabled
hermes: enabled
```

This reproduction follows the steps in https://github.com/software-mansion/react-native-svg/blob/main/USAGE.md#use-with-svg-files to enable direct importing of svg assets as react-native-svg components.

To reproduce crash:

1. Update contents of `broken-svg.svg` to contain svg source that triggers the crash
2. Run `npx react-native start --reset-cache`
3. Run `npm run android`
4. Verify the app crashes on launch, you can view the cause in Android Studio logcat.
