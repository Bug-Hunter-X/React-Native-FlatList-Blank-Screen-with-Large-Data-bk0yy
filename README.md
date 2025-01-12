# React Native FlatList Blank Screen Issue

This repository demonstrates a common issue in React Native where a FlatList component renders a blank screen when provided with a large dataset. The issue arises from performance bottlenecks and how React Native handles large lists.

## Problem

A React Native app using FlatList to display a large array of data renders a blank screen instead of displaying the list items. This is usually because of the extensive rendering time required by React Native for large datasets.  The solution involves optimizing rendering with techniques like windowing, pagination, or virtualization.

## Solution

The solution provided utilizes `windowSize` prop of the `FlatList` to efficiently render a subsection of the list at any given time.  This method avoids rendering the entire list at once, significantly improving performance and preventing the blank screen issue.

## Reproduction Steps

1. Clone the repository.
2. Run `npm install` or `yarn install` to install dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to start the app.
4. Observe the initial blank screen (bug) before scrolling. 
5. Scroll and observe improved rendering (solution).