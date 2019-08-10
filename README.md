# react-native-kill-app
Exit / Close / Kill / shutdown your react native app. Does not invoke a **crash** notification.

[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/Kennytian/react-native-exit-app/pulls)
[![npm](https://img.shields.io/npm/v/react-native-kill-app.svg?style=flat-square)](https://www.npmjs.com/package/react-native-kill-app)
[![Downloads](https://img.shields.io/npm/dm/react-native-kill-app.svg?style=flat-square)](https://www.npmjs.com/package/react-native-kill-app)
[![GitHub contributors](https://img.shields.io/github/contributors/Kennytian/react-native-exit-app.svg?style=flat-square)](https://github.com/Kennytian/react-native-exit-app/graphs/contributors)
[![GitHub last commit](https://img.shields.io/github/last-commit/Kennytian/react-native-exit-app.svg?style=flat-square)](https://github.com/Kennytian/react-native-exit-app/commits/master)
![Platform - Android and iOS](https://img.shields.io/badge/platform-Android%20%7C%20iOS-yellow.svg?style=flat-square)
[![HitCount](http://hits.dwyl.io/Kennytian/react-native-kill-app.svg)](http://hits.dwyl.io/Kennytian/react-native-kill-app)

>Support Xcode project with CocoasPod

>Support TypeScript TSX syntax

NOTICE:
- for React Native > 0.47 use react-native-kill-app >=1.x.x
- for React Native < 0.47 use react-native-kill-app <1.x.x

## Setup

Fast and easy:
```bash
yarn add react-native-kill-app
react-native link react-native-kill-app
```

Or manual: add the latest version as dependency to your package.json.

```javascript
{
  "name": "YourProject",
  ...
  },
  "dependencies": {
    ...
    "react-native-kill-app": "1.0.4",
    ...
  }
```

#### iOS

##### Add to Podfile

pod 'react-native-kill-app', :path => '../node_modules/react-native-kill-app'

##### Add to Frameworks
* Add RNExitApp.xcoderproj into your project in the Libraries folder.
* Add the .a file on the General tab of your target under Linked Frameworks And Libraries
* Add the .a file on the Build Phases tab of your target under Link Binary With Libraries

#### Android
* In the settings.gradle
  ```
    include ':react-native-kill-app', ':app'
    project(':react-native-kill-app').projectDir = new File(rootProject.projectDir, '../node_modules/react-native-kill-app/android')
  ```
* In the build.gradle
  ```
    compile project(':react-native-kill-app')
  ```
* In MainApplication.java
  ```
    import com.github.wumke.RNExitApp.RNExitAppPackage;
    ...
    @Override
    protected List<ReactPackage> getPackages() {
      return Arrays.<ReactPackage>asList(
        ...
        new RNExitAppPackage(),
        ...
      );
    }
    ...
  ```
## Usage

```javascript
import RNExitApp from 'react-native-kill-app';
...
RNExitApp.exitApp();
...
```

## Thanks

https://github.com/wumke/react-native-exit-app
