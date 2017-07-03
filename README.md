## UnityWithWebRTC
Unity using WebRTC UWP Libraries

This is a Unity Project with integration Plugins to utilize the UWP WebRTC Library from Nuget.Org.
Uses https://github.com/webrtc-uwp/PeerCC as reference for the integration project.

## Setup

* Install Unity 5.6.1f1
* Install Visual Studio 2017
* Clone this Project

Compiled plugin DLL’s are included in the Unity Project.
Plugin Source Code located in /External/Plugins.

## Known Issues

* Unity Peer Application only receives video/audio feed from transmitting peer.  Webcam/Mic is activated as required by UWP WebRTC Lib
* The plugin can be optimized further by using shaders to handle the color conversion


## Notes

A brief description of the InterOp in the project is at [Microsoft Real Life Code: Revisiting InterOp with Unity, UWP and DirectX]( https://www.microsoft.com/reallifecode/2017/06/28/revisiting-interop-unity-uwp-directx/)
