# ApplicationLoader-Error
A lot of errors can occurs during Application submission !


**ERROR ITMS-9000**<br>
- Message: The bundle 'com.xxxxxa' at bundle path 'Payload/xxxx.app' is not signed using an Apple submission certificate." at SoftwareAssets/SoftwareAsset (MZItmspSoftwareAssetPackage)<br>
- Solution:??

**ERROR ITMS-90017**<br>
- Message: this bundle is invalid.the IPA format requires a top-level directory named Payload, containing only a.app bundle and optional plugins in a PLUGINS directory.
- Solution:??

**ERROR ITMS-90023**<br>
- Message: Missing required icon file.  The bundle does not contain an app icon for iPad of exactly '72x72' pixels, in .png format for iOS versions < 7.0.
- Solution:??

**ERROR ITMS-90035**<br>
- Message: Invalid Signature. Invalid signature (code or signature have been modified). Make sure you have signed your application with a distribution certificate, not an ad hoc certificate or a development certificate. Verify that the code signing settings in Xcode are correct at the target level (which override any values at the project level). Additionally, make sure the bundle you are uploading was built using a Release target in Xcode, not a Simulator target. If you are certain your code signing settings are correct, choose "Clean All" in Xcode, delete the "build" directory in the Finder, and rebuild your release target. For more information, please consult https://developer.apple.com/library/ios/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html
- Solution:??
        
**ERROR ITMS-90046**<br>
- Message: Invalid Code Signing Entitlements. Your application bundle's signature contains code signing entitlements that are not supported on iOS. Specifically, value '*' for key 'com.apple.developer.associated-domains' in 'Payload/appomcom.app/appomcom' is not supported. <br>
- Solution:??

**ERROR ITMS-90098**<br>
- Message: This bundle is invalid. The key UIRequiredDeviceCapabilities contains value 'arm64' which is incompatible with the MinimumOSVersion value of '8.0'.<br>
- Solution: The Info.plist of the app may no values for the key "UIRequiredDeviceCapabilities" contain "that would prevent the opening of this app on iOS devices. For more information, see the information on the key "UIRequiredDeviceCapabilities".

**ERROR ITMS-90125**<br>
- Message: the binary is invalid. the encryption info in the lc_encryption_info load command is either missing or invalid, or the binary is already encrypted
- Solution:??

**ERROR ITMS-90164**<br>
- Message: Invalid Code Signing Entitlements. The entitlements in your app bundle signature do not match the ones that are contained in the provisioning profile. According to the provisioning profile, the bundle contains a key value that is not allowed: 'TEAMID.com.Company.CompanyApp' for the key 'application-identifier' in 'Payload/CompanyApp.app/CompanyApp<br>
- Solution:??

**ERROR ITMS-90206**<br>
- Message: Invalid Bundle. The bundle at 'MyApp.app/PlugIns/MyAppShare.appex' contains disallowed file 'Frameworks'.
- Solution:??

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
