---
title: Try Flutter
date: 2021-04-09 20:39:03
tags: Flutter
---

## Get started
- get SDK 👉[Flutter SDK releases](https://flutter.dev/docs/development/tools/sdk/releases)
- update system path
- ![](/images/tryflutter/Snipaste_2021-04-09_20-44-44.png)
- update user path
- ![](/images/tryflutter/Snipaste_2021-04-09_20-45-40.png)
- ![](/images/tryflutter/Snipaste_2021-04-09_20-46-04.png)
- ` flutter doctor`
- ![](/images/tryflutter/Snipaste_2021-04-09_20-50-12.png)
- 👉[Android Studio](https://developer.android.com/studio/index.html)
<!-- more -->

## First Go
- `flutter create projectname`
- `code ./` open by vscode
- `flutter doctor` re-examined
- ![](/images/tryflutter/Snipaste_2021-04-10_01-17-04.png)
- `flutter emulator` check emulator
- ![](/images/tryflutter/Snipaste_2021-04-10_01-18-32.png)
- `flutter emulators --launch Pixel_3a_API_30_x86` run the emulator
- ![](/images/tryflutter/Snipaste_2021-04-10_01-19-50.png)
- `flutter run` or `flutter run -d <emulatorId>`
- ![](/images/tryflutter/Snipaste_2021-04-10_01-27-37.png)

## Get lib
- 👉[pub.dev](https://pub.dev/)
- 在项目目录下 pubspec.yaml 里加入依赖和版本号
```yaml
dependencies:
  flutter:
    sdk: flutter
  intl: ^0.17.0

  # The following adds the Cupertino Icons font to your application.
  # Use with the CupertinoIcons class for iOS style icons.
  cupertino_icons: ^1.0.2

dev_dependencies:
  flutter_test:
    sdk: flutter
```
- 保存即可，或者到 console 执行 `flutter packages get`

## In process
### Could not receive a message from the daemon.
- ![](/images/tryflutter/Snipaste_2021-05-03_00-54-16.png)
- 关闭共享的网络即可 👉[Could not receive a message from the daemon](https://stackoverflow.com/questions/49609313/could-not-receive-a-message-from-the-daemon)
- ![](/images/tryflutter/Snipaste_2021-05-03_00-58-11.png)

