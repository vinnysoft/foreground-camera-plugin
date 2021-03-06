# Foreground Camera Plugin for Phonegap (Cordova) #

The default Phonegap (Cordova) Camera Plugin calls the native camera and this makes Android Garbage Collector to kill background applications. This plugin avoid your application to go background and be killed by Garbage Collector with other applications. We used the Phonegap source code and modified it to avoid this problem. This plugin works only with File URI.

## Contributions ##

We need help to upgrade this plugin as Cordova evolves. Developers are welcome.
Contact if you want to help us to maintain and grow up this plugin! :)

## Donations ##

[![](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=WK4N5FLJLGXV6)

## Releases ##

|**Phonegap (Cordova)**|**Foreground Camera Plugin**|
|:---------------------|:---------------------------|
|2.4.0|1.4|
|2.1.0|1.3|
|1.8.0|1.1|

## Download ##

Please see: https://github.com/vinnysoft/foreground-camera-plugin/releases

## Adding the plugin to your project ##
1) To install the plugin, move the file **camera.js** to your project's www folder and include a reference to it in your html files.
<br />2) Put the Java files in your **src/** folder.
<br />3) Change the default Camera Plugin into **res/xml/config.xml** file to:
```
<plugin name="Camera" value="<path to your ForegroundCameraLauncher.java>"/>
```
4) Put the **strings.xml** in your res/values folder.
<br />5) Put the **foregroundcameraplugin.xml** in your res/layout folder.
<br />6) Put **cordova-X.X.X.jar** file in your /lib folder.
<br />7) In your **AndroidManifest.xml**, put these permissions:
```
    <uses-permission android:name="android.permission.CAMERA" />
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

    <uses-feature android:name="android.hardware.camera" />
    <uses-feature android:name="android.hardware.camera.autofocus" />
```
8) Declare the Camera Activity:
```
<activity android:name=".CameraActivity" 
android:label="ForegroundCameraPlugin"
android:screenOrientation="landscape"> </activity>
```
## Using the plugin ##

See the sample project.

## License ##
#### Licensed under Apache License 2.0: ####


```
/**
 *  Copyright 2013 Bruno Carreira - Lucas Farias - Rafael Luna - Vinícius Fonseca
 *
 *  Licensed under the Apache License, Version 2.0 (the "License");
 *  you may not use this file except in compliance with the License.
 *  You may obtain a copy of the License at
 *
 *      http://www.apache.org/licenses/LICENSE-2.0
 *
 *  Unless required by applicable law or agreed to in writing, software
 *  distributed under the License is distributed on an "AS IS" BASIS,
 *  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 *  See the License for the specific language governing permissions and
 *  limitations under the License.
 */
```
