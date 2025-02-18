---
title: Deep Links
hide_title: true
displayed_sidebar: react-native
---

# How to enable Deep Links in your apps

To be able to use some wallets in your application, they require a way to redirect back to your app via deep linkin. This short guide will give the practical steps to achieve it on both Android and iOS.

If you want to learn more about deep linking please check the official documentation for [Android](https://developer.android.com/training/app-links/deep-linking) and [iOS](https://developer.apple.com/ios/universal-links/).

## Android

The short version is that you need to tell the Android OS that your application can manage certain urls. You define this URL in your `AndroidManifest.xml` and when another app (e.g. a wallet) asks the Android OS to open the url, the OS will check which apps can open it and send you the request.

Open your `AndroidManifest.xml` and add the following code inside your main `<activity>` block:

```
<activity
    android:name="com.example.android.GizmosActivity"
    <intent-filter>
        <action android:name="android.intent.action.VIEW" />
        <category android:name="android.intent.category.DEFAULT" />
        <category android:name="android.intent.category.BROWSABLE" />
        <data android:scheme="your.scheme" />
    </intent-filter>
</activity>
```

To understand how this works, please refer to the [Android's developer official documentation.](https://developer.android.com/training/app-links/deep-linking)

## iOS

Open your `Info.plist` file and add a new `CFBundleURLTypes` key:

```
<key>CFBundleURLTypes</key>
	<array>
		<dict>
			<key>CFBundleURLSchemes</key>
			<array>
				<string>your.scheme</string>
			</array>
		</dict>
	</array>
```

Next, open your `AppDelegate.mm` file and import the `RCTLinkingManager` header file and add the following method:

```
#import <React/RCTLinkingManager.h>

...

// Linking API
- (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<UIApplicationOpenURLOptionsKey,id> *)options {
  return [super application:application openURL:url options:options] || [RCTLinkingManager application:application openURL:url options:options];
}
```

To understand how this works, please refer to the [iOS's developer official documentation.](https://developer.apple.com/ios/universal-links/)
