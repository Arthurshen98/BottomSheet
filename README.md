[apk-url]:          https://github.com/michaelbel/BottomSheet/raw/master/app/release/bottomsheet-v1.2.3.apk
[wiki-url]:         https://github.com/michaelbel/BottomSheet/wiki/usage
[paypal-url]:       https://paypal.me/michaelbel
[github-url]:       https://github.com/michaelbel/bottomsheet
[licence-url]:      http://www.apache.org/licenses/LICENSE-2.0
[bintray-url]:      https://bintray.com/michael-bel/maven/bottomsheet/_latestVersion
[arsenal-url]:      https://android-arsenal.com/details/1/6623
[mdguides-url]:     https://material.io/guidelines/components/bottom-sheets.html#
[googleplay-url]:   https://play.google.com/store/apps/details?id=org.michaelbel.bottomsheetdialog
[methodscount-url]: http://www.methodscount.com/?lib=org.michaelbel%3Abottomsheet%3A1.1.2

[launcher-path]: ../master/app/src/main/res/mipmap-xxxhdpi/ic_launcher.png

[ide-badge]:          https://img.shields.io/badge/Android_Studio-3.1.4-009688.svg
[minsdk-badge]:       https://img.shields.io/badge/minSdkVersion-21-009688.svg
[paypal-badge]:       https://img.shields.io/badge/Donate-Paypal-009688.svg
[license-badge]:      https://img.shields.io/badge/License-Apache_v2.0-009688.svg
[arsenal-badge]:      https://img.shields.io/badge/Android%20Arsenal-BottomSheet-009688.svg?style=flat
[bintray-badge]:      https://api.bintray.com/packages/michael-bel/maven/bottomsheet/images/download.svg
[platform-badge]:     https://img.shields.io/badge/Platform-Android-009688.svg
[googleplay-badge]:   https://img.shields.io/badge/Google_Play-Demo-009688.svg
[methodscount-badge]: https://img.shields.io/badge/Methods_and_Size-355_%20%7C%20_55KB-009688.svg

<!------------------------------------------------------------------------------------------------------------------------------------->

[![Launcher][Launcher-path]][github-url]
# BottomSheet
[![Bintray][bintray-badge]][bintray-url]
[![Platform][platform-badge]][github-url]
[![MinSdk][minsdk-badge]][github-url]
[![IDE][ide-badge]][github-url]
[![License][license-badge]][licence-url]
[![AndroidArsenal][arsenal-badge]][arsenal-url]
[![GooglePlay][googleplay-badge]][googleplay-url]
[![Methodscount][methodscount-badge]][methodscount-url]
[![Paypal][paypal-badge]][paypal-url]

BottomSheet dialogs library for Android with [material design concept][mdguides-url].
Bottom sheets slide up from the bottom of the screen to reveal more content.

<div style="dispaly:flex">
    <img style="margin-left:0px;" src="/art/screens/light_1.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/light_2.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/light_3.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/light_4.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/dark_1.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/dark_2.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/dark_3.png" width="24%">
    <img style="margin-left:0px;" src="/art/screens/dark_4.png" width="24%">
</div>

<div style="dispaly:flex;">
    <img style="margin-left:0px;" src="/art/screens/light_landscape.png" width="49%">
    <img style="margin-left:0px;" src="/art/screens/dark_landscape.png" width="49%">
</div>    

## Demo
<a href="https://play.google.com/store/apps/details?id=org.michaelbel.bottomsheetdialog" target="_blank">
  <img alt="App on Google Play" src="https://goo.gl/cR2qQH" height="100"/>
</a>

Or [Download APK][apk-url].

## Download
```gradle
dependencies {
    implementation 'org.michaelbel:bottomsheet:1.2.3'
}
```

## Usage
```java
BottomSheet.Builder builder = new BottomSheet.Builder(context);
builder
   .setTitle(CharSequence title)
   .setItems(CharSequence[] items, Drawable[] icons, DialogInterface.OnClickListener listener)
   .setMenu(@MenuRes int menuResId, DialogInterface.OnClickListener listener)
   .setView(@LayoutRes int layoutResId)
   .setContentType(@BottomSheet.Type int type)
   .setDarkTheme(boolean darkTheme)
   .setFullWidth(boolean fullWidth)
   .setCellHeight(int cellHeightDp)
   .setDividers(boolean dividers)
   .setWindowDimming(@Range(from = 0, to = 255) int windowDimming)
   .setTitleMultiline(boolean multiline)
   .setFabBehavior(FloatingActionButton button)
   .setFabBehavior(FloatingActionButton button, @BottomSheet.FabBehavior int fabBehavior)
   .setBackgroundColor(@ColorInt int color)
   .setBackgroundColorRes(@ColorRes int color)
   .setTitleTextColor(@ColorInt int color)
   .setTitleTextColorRes(@ColorRes int color)
   .setItemTextColor(@ColorInt int color)
   .setItemTextColorRes(@ColorRes int color)
   .setIconColor(@ColorInt int color)
   .setIconColorRes(@ColorRes int color)
   .setItemSelector(int selector);
   .setOnShowListener(new DialogInterface.OnShowListener() {
       @Override
       public void onShow(DialogInterface dialog) {
       }
   });
   .setOnDismissListener(new DialogInterface.OnDismissListener() {
       @Override
       public void onDismiss(DialogInterface dialog) {
       }
   });
   .setCallback(new BottomSheetCallback() {
       @Override
       public void onShown() {
       }
       
       @Override
       public void onDismissed() {
       }
   })
   .show();
```

## Wiki
For all information check [BottomSheet Wiki][wiki-url].

## License

    Copyright 2016-2018 Michael Bel

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
