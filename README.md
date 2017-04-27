# ApplicationLoader-Error
A lot of errors can occurs during Application submission !

**ERROR ITMS-4238**<br>
- Message: Redundant Binary Upload
 ```
 Solution: change the build version or app version
 ```

**ERROR ITMS-9000**<br>
- Message: The bundle 'com.xxxxxa' at bundle path 'Payload/xxxx.app' is not signed using an Apple submission certificate." at SoftwareAssets/SoftwareAsset (MZItmspSoftwareAssetPackage)<br>
```
Solution: Are you sure to use the good certificate to sign?
```

**ERROR ITMS-90017**<br>
- Message: this bundle is invalid.the IPA format requires a top-level directory named Payload, containing only a.app bundle and optional plugins in a PLUGINS directory.
```
Solution: Bad format ? Invalid structure?
/Payload/a.app
/Payload/Plugins
```

**ERROR ITMS-90022**<br>
- Message : Missing required icon file. The bundle does not contain an app icon for iPhone / iPod Touch of exactly '120x120' pixels, in .png format for iOS versions >= 7.0.
```
Solution: Add missing icons in your appiconset
```

**ERROR ITMS-90023**<br>
- Message : Missing required icon file.  The bundle does not contain an app icon for iPad of exactly '72x72' pixels, in .png format for iOS versions < 7.0.
- Message : Missing required icon file. The bundle does not contain an app icon for iPad of exactly '76x76' pixels, in .png format for iOS versions >= 7.0
- Message: Missing required icon file. The bundle does not contain an app icon for iPad of exactly '167x167' pixels, in .png format .
```
Solution: Add missing icons in your appiconset
```

**ERROR ITMS-90035**<br>
- Message: Invalid Signature. Invalid signature (code or signature have been modified). Make sure you have signed your application with a distribution certificate, not an ad hoc certificate or a development certificate. Verify that the code signing settings in Xcode are correct at the target level (which override any values at the project level). Additionally, make sure the bundle you are uploading was built using a Release target in Xcode, not a Simulator target. If you are certain your code signing settings are correct, choose "Clean All" in Xcode, delete the "build" directory in the Finder, and rebuild your release target. For more information, please consult https://developer.apple.com/library/ios/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html
```
Solution: ??
```

**ERROR ITMS-90046**<br>
- Message: Invalid Code Signing Entitlements. Your application bundle's signature contains code signing entitlements that are not supported on iOS. Specifically, value '*' for key 'com.apple.developer.associated-domains' in 'Payload/appomcom.app/appomcom' is not supported. <br>
```
Solution: ??
```

**ERROR ITMS-90096**<br>
- Message: Your binary is not optimized for iPhone 5 - New iPhone apps and app updates submitted must support the 4-inch display on iPhone 5 and must include a launch image referenced in the Info.plist under UILaunchImages with a UILaunchImageSize value set to {320, 568}. Launch images must be PNG files and located at the top-level of your bundle, or provided within each .lproj folder if you localize your launch images. Learn more about iPhone 5 support and app launch images by reviewing the 'iOS Human Interface Guidelines' at 'https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/MobileHIG/IconsImages/IconsImages.html#//apple_ref/doc/uid/TP40006556-CH14-SW5' and the 'iOS App Programming Guide' at 'https://developer.apple.com/library/ios/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/App-RelatedResources/App-RelatedResources.html#//apple_ref/doc/uid/TP40007072-CH6-SW12'.
```
Solution: Read the documentation and add missing ressources
```

**ERROR ITMS-90098**<br>
- Message: This bundle is invalid. The key UIRequiredDeviceCapabilities contains value 'arm64' which is incompatible with the MinimumOSVersion value of '8.0'.<br>
```
Solution: The Info.plist of the app may no values for the key "UIRequiredDeviceCapabilities" contain "that would prevent the opening of this app on iOS devices. For more information, see the information on the key "UIRequiredDeviceCapabilities".
```

**ERROR ITMS-90125**<br>
- Message: the binary is invalid. the encryption info in the lc_encryption_info load command is either missing or invalid, or the binary is already encrypted
```
Solution: ??
```

**ERROR ITMS-90164**<br>
- Message: Invalid Code Signing Entitlements. The entitlements in your app bundle signature do not match the ones that are contained in the provisioning profile. According to the provisioning profile, the bundle contains a key value that is not allowed: 'TEAMID.com.Company.CompanyApp' for the key 'application-identifier' in 'Payload/CompanyApp.app/CompanyApp<br>
```
Solution: ??
```

**ERROR ITMS-90206**<br>
- Message: Invalid Bundle. The bundle at 'MyApp.app/PlugIns/MyAppShare.appex' contains disallowed file 'Frameworks'.
```
Solution: ??
```

**ERROR ITMS-90347**<br>
- Message: "Bad bundle identifier. The bundle identifier 'com.jmo.touchup.today.proxymity' of the application extension XXX.app/PlugIns/YYYY.appex should start with the application's bundle identifier 'com.jmo.xxx' and not contain more than one period “.” after the application's bundle ID.""

```
Solution: Damned ! Your have to change your bundleId and generate your mobile provisionning !
```

**ERROR ITMS-90394**<br>
- Message: "Missing Icon. The watch application 'XXXXX' is missing icon with name pattern 'XXX.png' ). Please visit https://developer.apple.com/watchkit/ for more information."

```
Solution: Add the missing icon in your assets
```

**ERROR ITMS-90474**<br>
- Message: Bundle Invalid. iPad Multitasking support requires there orientations: 'UIInterfaceOrientationPortrait,UIIinterfaceOrientationPortraitUpsideDown,UIInterfaceOrientationLandscapeLeft,UIInterfaceOrientationLandscapeRight'. Found 'UIInterfaceOrientationPortrait' in bundle.<br>
- Solution: info.plist need the configuration of "Requires full screen"
Add UIRequiresFullScreen key and value true/false depending on your app multitasking support
```xml
<key>UIRequiresFullScreen</key>
<true/>
```

**ERROR ITMS-90475**<br>
- Message: Invalid Bundle. iPad Multitasking support requires launch story board in bundle ‘appname’
- Solution: info.plist need the configuration of "Requires full screen"<br>
Add UIRequiresFullScreen key and value true/false depending on your app multitasking support
```xml
<key>UIRequiresFullScreen</key>
<true/>
```
**ERROR ITMS-90502**<br>
- Message: Invalid Bundle. Apps that only contain the arm64 slice must also have 'arm64' in the list of UIRequiredDeviceCapabilities in Info.plist."<br>
- Solution:??

**ERROR ITMS-90640**<br>
- Message: Invalid Info.plist value. Invalid Info.plist value. The value for key UIApplicationShortcutWidget must be the bundle identifier of a Today extension in the app.<br>
- Solution:Change the value of UIApplicationShortcutWidget in your info.plist
```xml
<key>UIApplicationShortcutWidget</key>
<string>YOUR_WIDGET_BUNDLE_ID</string>
```
**WARNING ITMS-90703**<br>
- Message: "Deprecated Xcode Build. Due to resolved app archives issues, we will be deprecating Xcode 8.3 on May 10, 2017, at which time app archives built with 8.3 will no longer be accepted by the App Store. Download Xcode 8.3.2 or newer, rebuild your app and resubmit."
```xml
Migrate your project to Xcode 8.3.2, compile, cross the fingers and upload
```
