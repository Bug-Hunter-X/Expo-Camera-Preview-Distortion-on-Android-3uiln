# Expo Camera Preview Distortion on Android

This repository demonstrates a bug in the Expo Camera API where the preview image can be distorted on Android devices when using certain aspect ratios.  The captured image itself is unaffected; the problem lies solely in the preview display.

## Bug Description
The preview image in the `Camera` component may appear stretched or compressed, especially on devices with different screen densities.  The issue seems tied to how aspect ratios are calculated and handled, particularly in conjunction with screen orientation changes.

## Steps to Reproduce
1. Clone this repository.
2. Run the app on an Android device (emulator or physical).
3. Observe the preview image within the `Camera` component. Distortion will likely be visible.

## Solution
The solution provided attempts to calculate and apply corrections for different screen densities. There is still a chance that the preview is slightly off, because this problem may depend on the particular device's characteristics.