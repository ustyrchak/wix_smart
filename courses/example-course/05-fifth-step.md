# Environment setup

## Automatic or manual setup
For automatic env setup on Mac follow [this article](https://github.com/wix-private/mobile-ecosystem/blob/master/packages/shono/commands/shono-onboard/README.md).

Please, note that XCode may need to be downloaded manually.

Also, the automatic setup might not start on a clean machine with the default (public) npm registry. In this case, run this command first:
```bash
yarn config set npmRegistryServer https://npm.dev.wixpress.com
```

In case of any issues with automatic setup, follow this [manual setup](https://github.com/wix/react-native-crash-course/blob/master/docs/Basics.enviromentSetup.md).
Pay attention to the added notes below for specific instructions which we couldn't publish in the OSS article.

## Verify

Verify RN setup via [creating a new app](https://reactnative.dev/docs/environment-setup#creating-a-new-application) and then [running it](https://reactnative.dev/docs/environment-setup#running-your-react-native-application)

#### Known issues

`Issue 1`. Credit Viktorija

If the build is failing both in Terminal and Xcode and you see this error:

```
Undefined symbols for architecture x86_64: "\_\_\_darwin_check_fd_set_overflow", referenced from: \_RAND_poll in libcrypto.a(rand_unix.o)
```

`Solution`

1. Initialize React Native project using RC 0.63.3: "react-native init newproject --version 0.63.3"
2. Open "newproject/ios/Podfile". Lock OpenSSL-Universal version. Add this to Podfile (e.g. in target newproject section): "pod 'OpenSSL-Universal', '1.0.2.19'"
3. Do "pod install" and continue as specified in guide

## Android Studio

In the CI, we don’t have Android Studio so you can use any version. However at Wix, we’re using Gradle to run the Android builds, so make sure you have the latest Android Studio.

## Software licenses

Feel free to [open a Jira ticket](https://jira.wixpress.com/secure/Dashboard.jspa) under "Wix IT" project for any software license you wish to use (WebStorm, Wallaby etc.)
