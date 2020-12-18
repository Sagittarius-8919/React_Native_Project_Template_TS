# React_Native_Project_Template_TS

https://reactnative.dev/blog/2017/03/13/introducing-create-react-native-app
https://reactnative.dev/blog/2018/05/07/using-typescript-with-react-native :

npm i -g create-react-native-app
create-react-native-app my-project
cd my-project

 "android": "react-native run-android",
    "ios": "react-native run-ios",
    "start": "react-native start",
    "test": "jest",
    "lint": "eslint .",
    "emulator-android": "emulator -avd Pixel_2_API_29",
    "menu-android-device": "adb shell input keyevent 82",
    "android-reverse-port": "adb reverse tcp:8081 tcp:8081",
    "reload-android-device": "adb shell input text \"RR\"",
    "make-apk-mac": "cd android && ./gradlew assembleRelease",
    "install-apk": "cd android/app/build/outputs/apk/release/ && adb -d install app-release.apk",
    "uninstall-apk": "cd android && adb uninstall com.connections_app",
    "make-aab-mac": "cd android && ./gradlew bundleRelease",
    "android-clean-mac": "cd android && ./gradlew clean",
    "android-bundle": "react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/build/intermediates/res/merged/release/",
    "postinstall": "jetifier -r"

yarn add --dev typescript
yarn add --dev react-native-typescript-transformer
yarn tsc --init --pretty --jsx react
touch rn-cli.config.js
yarn add --dev @types/react @types/react-native

To rn-cli.config.js:
module.exports = {
  getTransformModulePath() {
    return require.resolve('react-native-typescript-transformer');
  },
  getSourceExts() {
    return ['ts', 'tsx'];
  }
};

https://stackoverflow.com/a/61913747
distributionUrl=https\://services.gradle.org/distributions/gradle-6.3-all.zip



