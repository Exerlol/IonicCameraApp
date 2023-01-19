# IonicCameraApp
Created with minimum amount of code necessary to recreate the camera permission issue

## Installation and running app locally inside of browser:
1. Run `npm install` in order to install all necessary dependencies
2. Run `ionic serve` and navigate to `http://localhost:4200/`

## Issue with camera permission repro steps:
1. Run `ionic build`
2. Run `ionic cap add android`
3. Connect android device with Android 12
4. Run `npx cap run android --external -livereload` to run app on connected android device
5. Click on "Camera button" in the middle of the screen
6. When prompted click "Don't allow"

Result: 
  Camera will open and you will be able to take a picture on device
Expected: 
  Camera shouldn't open since user rejected camera permission
