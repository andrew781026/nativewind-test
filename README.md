This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

# Getting Started

>**Note**: Make sure you have completed the [React Native - Environment Setup](https://reactnative.dev/docs/environment-setup) instructions till "Creating a new application" step, before proceeding.

## Step 1: Start the Metro Server

First, you will need to start **Metro**, the JavaScript _bundler_ that ships _with_ React Native.

To start Metro, run the following command from the _root_ of your React Native project:

```bash
# using npm
npm start

# OR using Yarn
yarn start
```

## Step 2: Start your Application

Let Metro Bundler run in its _own_ terminal. Open a _new_ terminal from the _root_ of your React Native project. Run the following command to start your _Android_ or _iOS_ app:

### For Android

```bash
# using npm
npm run android

# OR using Yarn
yarn android
```

### For iOS

```bash
# using npm
npm run ios

# OR using Yarn
yarn ios
```

If everything is set up _correctly_, you should see your new app running in your _Android Emulator_ or _iOS Simulator_ shortly provided you have set up your emulator/simulator correctly.

This is one way to run your app — you can also run it directly from within Android Studio and Xcode respectively.

## Step 3: Modifying your App

Now that you have successfully run the app, let's modify it.

1. Open `App.tsx` in your text editor of choice and edit some lines.
2. For **Android**: Press the <kbd>R</kbd> key twice or select **"Reload"** from the **Developer Menu** (<kbd>Ctrl</kbd> + <kbd>M</kbd> (on Window and Linux) or <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (on macOS)) to see your changes!

   For **iOS**: Hit <kbd>Cmd ⌘</kbd> + <kbd>R</kbd> in your iOS Simulator to reload the app and see your changes!

## Congratulations! :tada:

You've successfully run and modified your React Native App. :partying_face:

### Now what?

- If you want to add this new React Native code to an existing application, check out the [Integration guide](https://reactnative.dev/docs/integration-with-existing-apps).
- If you're curious to learn more about React Native, check out the [Introduction to React Native](https://reactnative.dev/docs/getting-started).

# Troubleshooting

If you can't get this to work, see the [Troubleshooting](https://reactnative.dev/docs/troubleshooting) page.

# Learn More

To learn more about React Native, take a look at the following resources:

- [React Native Website](https://reactnative.dev) - learn more about React Native.
- [Getting Started](https://reactnative.dev/docs/environment-setup) - an **overview** of React Native and how setup your environment.
- [Learn the Basics](https://reactnative.dev/docs/getting-started) - a **guided tour** of the React Native **basics**.
- [Blog](https://reactnative.dev/blog) - read the latest official React Native **Blog** posts.
- [`@facebook/react-native`](https://github.com/facebook/react-native) - the Open Source; GitHub **repository** for React Native.

----------------

1. Create the project

```shell
npx react-native init AwesomeProject
cd AwesomeProject
```

You will need to install nativewind and it's peer dependency tailwindcss.

```shell
yarn add nativewind
yarn add --dev tailwindcss # change to "tailwindcss": "3.3.2",
```

2. Setup Tailwind CSS
   Run npx tailwindcss init to create a tailwind.config.js file

```shell
npx tailwindcss init # create a tailwind.config.js file
```

Add the paths to all of your component files in your tailwind.config.js file.

```diff
// tailwind.config.js

module.exports = {
- content: [],
+ content: ["./App.{js,jsx,ts,tsx}", "./<custom-folder>/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. Add the Babel plugin
   Modify your babel.config.js

```diff
// babel.config.js
module.exports = {
   presets: ['module:metro-react-native-babel-preset'],
+  plugins: ["nativewind/babel"],
};
```


# Steps to Get Start

1. install [openJDK 17](https://learn.microsoft.com/zh-tw/java/openjdk/download)
2. install [Android Studio](https://developer.android.com/studio?hl=zh-tw#get-android-studio)
3. (android) Setup %ANDROID_HOME% = %LOCALAPPDATA%\Android\Sdk
4. (java)    Setup %JAVA_HOME% = C:\Program Files\Microsoft\jdk-17.0.9.8-hotspot
5. (adb)     Setup Path = %LOCALAPPDATA%\Android\Sdk\platform-tools

```shell
set ANDROID_HOME=%LOCALAPPDATA%\Android\Sdk
set JAVA_HOME=C:\Program Files\Microsoft\jdk-17.0.9.8-hotspot
set Path=%Path%;%LOCALAPPDATA%\Android\Sdk\platform-tools
```

6. npm run start
