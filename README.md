# ApplicationLoader-Error
A lot of errors can occurs during Application submission !


**ERROR ITMS-9000**<br>
Message:The bundle 'com.xxxxxa' at bundle path 'Payload/xxxx.app' is not signed using an Apple submission certificate." at SoftwareAssets/SoftwareAsset (MZItmspSoftwareAssetPackage)<br>
Solution:??

**ERROR ITMS-90046**<br>
Message: Invalid Code Signing Entitlements. Your application bundle's signature contains code signing entitlements that are not supported on iOS. Specifically, value '*' for key 'com.apple.developer.associated-domains' in 'Payload/appomcom.app/appomcom' is not supported." <br>
Solution:??

**ERROR ITMS-90098**<br>
Message: This bundle is invalid. The key UIRequiredDeviceCapabilities contains value 'arm64' which is incompatible with the MinimumOSVersion value of '8.0'."<br>
Solution:??

**ERROR ITMS-90474**<br>
Message: Bundle Invalid. iPad Multitasking support requires there orientations: 'UIInterfaceOrientationPortrait,UIIinterfaceOrientationPortraitUpsideDown,UIInterfaceOrientationLandscapeLeft,UIInterfaceOrientationLandscapeRight'. Found 'UIInterfaceOrientationPortrait' in bundle.<br>
Solution: info.plist need the configuration of "Requires full screen"
Add UIRequiresFullScreen key and value true/false depending on your app multitasking support
```xml
<key>UIRequiresFullScreen</key>
<true/>
```

**ERROR ITMS-90475**<br>
Message: Invalid Bundle. iPad Multitasking support requires launch story board in bundle ‘appname’
Solution: info.plist need the configuration of "Requires full screen"<br>
Add UIRequiresFullScreen key and value true/false depending on your app multitasking support
```xml
<key>UIRequiresFullScreen</key>
<true/>
```
**ERROR ITMS-90502**<br>
Message: Invalid Bundle. Apps that only contain the arm64 slice must also have 'arm64' in the list of UIRequiredDeviceCapabilities in Info.plist."<br>
Solution:??
