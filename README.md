# Expo Image Component Local Image Loading Issue

This repository demonstrates a common, yet often overlooked, bug when using the Expo `Image` component with local image URIs.  The issue arises from incorrect handling of local image URIs, leading to the image failing to load.

## Problem
The `Image` component fails to render images if the `uri` prop isn't properly pre-processed to be Expo-compatible.

## Solution
Ensure that the image is properly loaded using the `Asset` API before using its URI with the `Image` component.  This ensures Expo's image loading mechanisms correctly handle the image path.

## Reproduction Steps
1. Clone this repository.
2. Run `expo start`.
3. Observe the broken image in `bug.js`.
4. Navigate to `bugSolution.js` to see the corrected implementation.