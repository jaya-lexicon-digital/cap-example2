# Read me

This initial app code was created with the below command from terminal:

ionic start --capacitor

Reference: https://capacitorjs.com/docs/getting-started/with-ionic

The app doesn't do much more as it was just created to test the CI using GitHub Action Workflows.

--------


Your Ionic app is ready! Follow these next steps:

- Go to your new project: cd ./ionic
- Run ionic serve within the app directory to see your app in the browser
- Run ionic capacitor add to add a native iOS or Android project using Capacitor
- Generate your app icon and splash screens using cordova-res --skip-config
  --copy
- Explore the Ionic docs for components, tutorials, and more:
  https://ion.link/docs
- Building an enterprise app? Ionic has Enterprise Support and Features:
  https://ion.link/enterprise-edition

# CI

The below guide was followed: https://dev.to/khromov/build-your-capacitor-android-app-bundle-using-github-actions-24do
to setup the Github Action Workflow for building the Android App Bundle .AAB

E.G https://github.com/jaya-lexicon-digital/cap-example2/actions/runs/1875811791

To convert the AAB to a APK for installation on actual device.

Refer:  
https://stackoverflow.com/questions/50419286/install-android-app-bundle-on-device
https://developer.android.com/studio/command-line/bundletool

E.G for MAC: 

brew install bundletool

bundletool build-apks --bundle=~/Downloads/app-release-signed.aab --output=~/Downloads/app-release-signed.apks

(*Open up Android Studio, emulator) 

adb devices 

bundletool install-apks --apks=~/Downloads/app-release-signed.apks


