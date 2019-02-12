# Popdeem Cordova Plugin
The Popdeem Cordova plugin allows you to use the Popdeem native iOS and Android SDKs inside your Cordova cross-platform application. Currently iOS and Android are supported

# Usage
## Add the plugin to your project
`cordova plugin add popdeem-cordova-plugin`

## Build the projects
`cordova build ios`
`cordova build android`

This will result in the PopdeemSDK pod being pulled into your iOS project, and the PopdeemSDK maven library being pulled into your Android project.

## Configuration

### iOS
See [Popdeem iOS SDK Documentation](http://popdeem-ios-docs.gitlab.io/#info-plist-additions) and complete the **info.plist additions** and **initialize SDK** steps. To do this you will need to locate the necessary files (`AppDelegate.m` & `projectname-info.plist`) in the iOS project generated by Cordova. This is the minimum needed to get up and running. 

Note: If you use native push notifications, the _Broadcast Features_ steps can also be completed.

### Android
See [Popdeem Android SDK Documentation](http://popdeem-android-docs.gitlab.io/#initialise-sdk) and complete the **AndroidManifest.xml additions** To do this you will need to locate the necessary file (`AndroidManifest.xml`)in the Android project generated by Cordova


## Popdeem Theme, Images & Strings
Create a `Popdeem` folder inside your cordova project. Include the images, strings & theme files provided for both iOS and Anrdoid.


## Social Login
To launch the social login popover from javascript, use the following:
`popdeem.enableSocialLogin(3, function() {}, function() {});`
The first parameter is the _numberOfPrompts_ argument. The popover is dismissible by the user - this argument denotes the maximum number of times a user can see this popover.


## Popdeem Home
To show the Popdeem Home flow from javascript, use the following:
`popdeem.pushPopdeemHome(function() {}, function() {});`. Popdeem Home encapsulates all of Popdeem’s functionality.


## Deliver Third Party Token
We may need you to deliver a user token. If so, you can do this by using this method:
`popdeem.deliverThirdPartyToken(“ThirdPartyToken", function() {}, function() {});`.

