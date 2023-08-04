## 

This is a demo app to demostrate windows native webrtc libs from WeiStreaming: WeiStreaming.WeiRtc.Native.lib.

It can establish a webrtc call with Google AppRtc Android demo app.

It can streaming from camera or desktop capture.

It has a built-in simple signaling server using direct TCP. When started, it run as a TCP server listening in port: 8888.

## Requirement for running the sample App.

1. Visual Studio 2019 Version 16.6.2 or later.
2. At least 8GB of RAM (16GB of RAM is recommended).
3. At least 15GB of disk space.
4. Windows x64 and 10 above
5. With two displays in order to better demo the desktop capture feature

## Build and Install Android AppRtc demo app

Download and build Google AppRtc Android demo app: https://github.com/njovy/AppRTCDemo

You can also build it from webrtc open source project: https://chromium.googlesource.com/external/webrtc/stable/talk/+/33ff0831ca67eeb4e33cfb4e0a0b68c6cc631ccc/examples/android/

You need to apply patches: android-weirtc-patch.patch. Copy android-weirtc-patch.patch to the root of Android AppRtc demo app code, then run following command.

```
 git am android-weirtc-patch.patch
```

Install on your device, and when started, type in your windows box's IP address that is running this demo app.

Go to Settings to give this app permission for camera and mic.

## Current Status

1. Able to Doing screen and camera capture
2. If test desktop capture, do the following change on file: WeiRtcApp.cpp

<img src="screen-share.jpg">

```
    _sample->AddVideoTrack(pipCanvas);
    //Open this line and commented out the top line to test desktop capture.
    //_sample->AddDesktopTrack(*_screenPipCanvas);
```

## Next steps

1. Tear down.
2. Add more track to existing connection.
3. Mesh call.













