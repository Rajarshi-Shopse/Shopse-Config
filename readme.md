# Shopse app initial configs

### Requirements
 -  node version `16.15.0`
 - gradle `7.3.3`
 - android sdk `30(min) - 34`
 - do all the necessary steps that is required for setting up react-native, [follow this link](https://reactnative.dev/docs/environment-setup)
 - install the platform-tools from android-studio and also add those to the `PATH`.
## Shopse-sales
 ### After setting up these things were needed
- copy these in the app leveled `build.gradle` into the dependencies
```gradle
implementation 'androidx.appcompat:appcompat:1.5.1'
implementation 'com.google.android.material:material:1.7.0'
```
- replace these into the android level `build.gradle` into the dependencies
```gradle
classpath("com.android.tools.build:gradle:7.1.1")
classpath("de.undercouch:gradle-download-task:5.0.1")
```
- delete `@amplitude/react-native`, the amplitude sdk for react-native and also remove the imports and uses in the files wherever it was used. 
- now go to `android` folder and do `./gradlew clean`.
- now come to the main folder by `cd ..` and run `npm run android` or `yarn android`.

## Shopse-Merchant
- do `npm install` 
- go to the `node_modules` and search for `react-native-qrcode-scanner`. go the `node_modules` of `react-native-qrcode-scanner` and delete the `react-native-permissions` folder.
- do `npm run android` and it will work
