# Create and run new project on Kiano Elegance 4.1
Today I Learned how to create a new react-native app an run it on my Kiano Elegance 4.1.

```bash
react-native init MyApp
cd MyApp
```

Then I edited file `~/Projects/ReactNative/MyApp/android/build.gradle`:
changed this line: `classpath 'com.android.tools.build:gradle:1.3.1'`
to: `classpath 'com.android.tools.build:gradle:1.2.3'`

Then: 
```bash
react-native run-android
react-native start
```
And in another terminal tab:
```bash
adb reverse tcp:8081 tcp:8081
```

## Troubleshooting 

### Getting error while `react-native start`
Helped restarting the computer.
