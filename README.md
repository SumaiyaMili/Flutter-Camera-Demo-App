<h1 align="center">Hi <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">, I'm Sumaiya Akter</h1>
<h3 align="center">Mobile application with Flutter</h3>
<h1>

## Quick Clean Cache
1. Open android studio Tools->Flutter->Clean
2. Go to File -> Invalidate Caches / Restart
3. Or open terminal run "flutter clean"
4. Remove pubspec.lock
5. Double check the Flutter SDK Path config correcty - https://tppr.me/qn6dP

Or open the terminal and try this script:
```
flutter clean
flutter pub cache repair
flutter pub get
```

Rebuild the project again

## Update Flutter to Channel Stable
1. Open termimal on Mac or CommandLine on Window:
   ```
   flutter channel stable
   flutter upgrade --force
   ```
2. Also run "flutter doctor" and fix all the issues
3. Update the Flutter SDK Path from Android Studio - https://tppr.me/qn6dP


## Fix build issue on iOS
1. Remove following files and folders (see this screenshot - https://tppr.me/vwqX0 ) 

       - Go to ios: remove Pods folder, Podfile and fodfile.lock, .symlink folder (this folder is hidden)
       - remove build folder

2. Open XCode, File > Workspace Settings > Select 'New Build System' - https://tppr.me/CRHLC
3. Open terminal (at ios folder) and run:
    ```
    pod cache clean --all
    pod repo update
    pod install
    
    // if you are using Fluxstore try to run 
    pod update OneSignal
    ```
4. Open Android Studio and run the green button - https://tppr.me/h3aTb  

## Fix build issue on Android
1. Go to to android folder and run
```
// mac os
./gradlew clean

// window os
gradlew.bat clean
```
2. Go to android folder and remove the .grade hidden folder 
2. Go the Android Studio and run the project again.