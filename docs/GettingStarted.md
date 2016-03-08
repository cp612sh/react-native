---
id: getting-started
title: Getting Started
layout: docs
category: Quick Start
permalink: docs/getting-started.html
next: getting-started-linux
---

## Requirements需求

1. OS X - This guide assumes OS X which is needed for iOS development.本指南假设OS X需要用来作为iOS开发的基本条件。
2. [Homebrew](http://brew.sh/) is the recommended way to install Watchman and Flow.是一种推荐方式用来安装Wathman和Flow。
3. Install [Node.js](https://nodejs.org/) 4.0 or newer.安装[Node.js](https://nodejs.org/) 4.0或更新的版本。
  - Install **nvm** with [its setup instructions here](https://github.com/creationix/nvm#installation). Then run `nvm install node && nvm alias default node`, which installs the latest version of Node.js and sets up your terminal so you can run it by typing `node`. With nvm you can install multiple versions of Node.js and easily switch between them.通过[nvm安装指南](https://github.com/creationix/nvm#installation) 安装 **nvm**。接着运行 `nvm install node && nvm alias default node`，这是用来安装最新的Node.js版本并且设置你的终端以便让你容果键入 `node` 来运行之。通过 nvm 你可以安装多个版本的 Node.js 并且在它们之间进行切换。
  - New to [npm](https://docs.npmjs.com/)? [npm](https://docs.npmjs.com/)的新人？
4. `brew install watchman`. We recommend installing [watchman](https://facebook.github.io/watchman/docs/install.html), otherwise you might hit a node file watching bug. `brew install watchman` 。我们推荐安装 [watchman](https://facebook.github.io/watchman/docs/install.html)，否则你可能面对一个node文件观察的缺陷。
5. `brew install flow`, if you want to use [flow](http://www.flowtype.org). `brew install flow`，如果你想要使用 [flow](http://www.flowtype.org)。

We recommend periodically running `brew update && brew upgrade` to keep your programs up-to-date.我们推荐周期性地运行 `brew update && brew upgrade` 来保持你的程序的更新。

## iOS Setup iOS 安装

[Xcode](https://developer.apple.com/xcode/downloads/) 7.0 or higher is required. It can be installed from the App Store. 需要[Xcode](https://developer.apple.com/xcode/downloads/) 7.0 或者更高。这可以从App Store进行安装。

## Android Setup 安卓安装

To write React Native apps for Android, you will need to install the Android SDK (and an Android emulator if you want to work on your app without having to use a physical device). See [Android setup guide](docs/android-setup.html) for instructions on how to set up your Android environment.要写安卓的RN应用，你会需要安装安卓的SDK（以及一个安卓模拟器，如果你不想在实际的设备上进行应用调试）。参见 [安卓安装指南](docs/android-setup.html)中如何设置你的安卓环境部分。

_NOTE:_ There is experimental [Windows and Linux support](docs/linux-windows-support.html) for Android development.

## Quick start 快速开始

Install the React Native command line tools:安装RN命令行工具

    $ npm install -g react-native-cli

__NOTE__: If you see the error, `EACCES: permission denied`, please run the command: `sudo npm install -g react-native-cli`. __注意__：如果你看到错误－`EACCES: permission denied`，请运行命令：`sudo npm install -g react-native-cli`。

Create a React Native project:创建一个RN项目：

    $ react-native init AwesomeProject


**To run the iOS app:运行iOS应用**

- `$ cd AwesomeProject`
- Open `ios/AwesomeProject.xcodeproj` and hit run in Xcode.打开 `ios/AwesomeProject.xcodeproj` 并且双击运行。
- Open `index.ios.js` in your text editor of choice and edit some lines.在你的文本编辑器中打开 `index.ios.js` 并且编辑一些代码。
- Hit ⌘-R in your iOS simulator to reload the app and see your change!在iOS模拟器中 ⌘-R 来重新加载应用并查看变化！

_Note: If you are using an iOS device, see the [Running on iOS Device page](docs/running-on-device-ios.html#content).注意：如果你使用一个iOS设备，参见 [在iOS设备上运行](docs/running-on-device-ios.html#content)_

**To run the Android app:运行安卓应用：**

- `$ cd AwesomeProject`
- `$ react-native run-android`
- Open `index.android.js` in your text editor of choice and edit some lines.在你的文本编辑器中打开 `index.android.js` 并且编辑一些代码。
- Press the menu button (F2 by default, or ⌘-M in Genymotion) and select *Reload JS* to see your change!点击菜单按钮（默认F2，或者在Genymotion中 ⌘-M ）并且选择 *Reload JS* 来查看更改！
- Run `adb logcat *:S ReactNative:V ReactNativeJS:V` in a terminal to see your app's logs在终端中运行 `adb logcat *:S ReactNative:V ReactNativeJS:V` 来查看你的应用的日志。

_Note: If you are using an Android device, see the [Running on Android Device page](docs/running-on-device-android.html#content).注意：如果你使用一个安卓设备，参见 [在安卓设备上运行](docs/running-on-device-android.html#content)。_

Congratulations! You've successfully run and modified your first React Native app.恭喜！你已经成功修改并运行你的第一个RN应用。

_If you run into any issues getting started, see the [troubleshooting page](docs/troubleshooting.html#content).如果你在运行过程中碰到问题，查看 [故障检测](docs/troubleshooting.html#content)_

## Adding Android to an existing React Native project将安卓添加到现有的RN项目中

If you already have a (iOS-only) React Native project and want to add Android support, you need to execute the following commands in your existing project directory:如果你已经有了（仅iOS）RN项目并且想要添加安卓支持，你需要执行在现有的项目目录下执行以下命令：

1. Update the `react-native` dependency in your `package.json` file to [the latest version](https://www.npmjs.com/package/react-native)在你的 `package.json` 文件中更新 `react-native` 到 [最新版本](https://www.npmjs.com/package/react-native)
2. `$ npm install`
3. `$ react-native android`
