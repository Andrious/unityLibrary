
You've unzipped this collection of folders and files.

Recognize the folders mirror the folders found in your Flutter project.

The most important folder, unityLibrary, should be placed in your Flutter project's android folder.

Note the files they include and open them find the changes you need to make.

It's stated in the Setup documentation: "Be sure you have at least one scene added to your build"

https://pub.dev/packages/flutter_unity_widget#setup

This was not done in this and yet it still runs the sample.

If you encounter errors, look trough the package's Troubleshooting first 

https://github.com/juicycleff/flutter-unity-view-widget#troubleshooting


If you want Unity in it's own activity as an alternative, open the android/app/src/main/AndroidManifest.xml and change the following:
(NOTE: It's already commented out in the AndroidManifest.xml file provided)

    <activity
        android:name="com.xraph.plugin.flutter_unity_widget.OverrideUnityActivity"
        android:theme="@style/UnityThemeSelector"
        android:screenOrientation="fullSensor"
        android:launchMode="singleTask"
        android:configChanges="mcc|mnc|locale|touchscreen|keyboard|keyboardHidden|navigation|orientation|screenLayout|uiMode|screenSize|smallestScreenSize|fontScale|layoutDirection|density"
        android:hardwareAccelerated="false"
        android:process=":Unity">
    <meta-data android:name="com.xraph.plugin.flutter_unity_widget.OverrideUnityActivity" android:value="true" />
    </activity>