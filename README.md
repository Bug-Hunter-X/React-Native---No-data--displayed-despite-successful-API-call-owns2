# React Native: 'No data' displayed despite successful API call

This repository demonstrates a common issue in React Native applications where the 'No data' message is displayed briefly, even after a successful API call and data retrieval. The issue arises due to the asynchronous nature of API calls and how the component's state updates during the rendering cycle.

The problem is that the data is fetched asynchronously, meaning the render cycle might complete before the data is available.  This issue is addressed by using the loading state and only rendering the data once it's available. This also includes error handling to provide a more robust user experience.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` (or `npx react-native run-ios`).
4. Observe the 'No data' message that briefly appears before the actual data is displayed.

## Solution

The solution involves carefully managing the state and rendering logic to account for the asynchronous nature of API calls. The solution file demonstrates how to show a 'Loading...' message before data is available, and how to handle potential errors during the API call.