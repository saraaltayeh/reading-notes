# React Native

React Native runs on React, a popular open source library for building user interfaces with JavaScript. To make the most of React Native, it helps to understand React itself. This section can get you started or can serve as a refresher course.

- We’re going to cover the core concepts behind React:

  - components
  - JSX
  - props
  - state

## Interactive examples

```javascript
import React from 'react';
import { Text, View } from 'react-native';

const YourApp = () => {
  return (
    <View style={{ flex: 1, justifyContent: "center", alignItems: "center" }}>
      <Text>
        Try editing me! 🎉
      </Text>
    </View>
  );
}

export default YourApp;
```

## Core Components and Native Components

React Native is an open source framework for building Android and iOS applications using React and the app platform’s native capabilities. With React Native, you use JavaScript to access your platform’s APIs as well as to describe the appearance and behavior of your UI using React components: bundles of reusable, nestable code.

![img](https://reactnative.dev/docs/assets/diagram_react-native-components.svg)

## Expo

Expo is an open-source npm package and framework for React Native projects. The expo package enables many important features for building and scaling an app like OTA updates, instantly sharing your app, and web support.

## Features

1. Expo Go

Expo Go is a free, open-source client for running React Native apps on Android and iOS without needing to build anything locally. It is available on the App Store and Google Play.
With Expo Go, you can run your projects on your own device faster than ever, and share those projects across your whole team without the need for addition code signing.
2. Expo SDK

The Expo SDK provides access to device and system functionality such as contacts, camera, gyroscope, GPS location, etc., in the form of packages. You can install any Expo SDK package using expo-cli with the expo install command.
3. native API
4. Prebuild
5. Expo CLI
