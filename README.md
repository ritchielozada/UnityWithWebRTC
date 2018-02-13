## UnityWithWebRTC
Unity using WebRTC UWP Libraries

This is a Unity Project with integration Plugins to utilize the UWP WebRTC Library from Nuget.Org.
Uses https://github.com/webrtc-uwp/PeerCC as reference for the integration project.

## Requirements

**Unity3D Development Workstation**
* Install Unity3D 2017.3.0f3
* Install Visual Studio 2017 Update to 15.5.6 with Unity Support
* Clone this Project
* Must have WebCam, Microphone, Audio Output

**Visual Studio Workstation**
* Install Visual Studio 2017 Update to 15.5.6 with Unity Support
* Clone this Project
* Must have WebCam, Microphone, Audio Output

Compiled plugin DLL’s are included in the Unity Assets Folder \\UnityWithWebRTC\\Assets\\Plugins\\WebRtcWrapper

Org.WebRtc.dll+Org.WebRtc.winmd WebRTC libraries wrapped by WebRtcWrapper.dll for use with Unity

Plugin Source Code located in \\ExternalProjects.

## Setup

1. Build the XAML Test App (Visual Studio Workstation)
  * Open the Visual Studio Solution: \\ExternalProjects\\WebRtcIntegration\\WebRtcIntegration.sln
  * Right-Click "XamlTestApp" in the Visual Studio Solution
  * Click Build and then Deploy to install the XamlTestApp on the workstation   
1. Build the Plugin DLL (Unity3D Development Workstation)
  * Open the Visual Studio Solution: \\ExternalProjects\\WebRtcIntegration\\WebRtcIntegration.sln
  * Build and Deploy the "WebRtcWrapper" Project, the DLL's are automatically copied to the Unity Asset Folder
1. Build the Unity Project (Unity3D Development Workstation)
  * Start Unity3D, select the clone root folder
  * Load the Scene "RenderTexture" located in \\Scenes\\RenderTexture
  * Open the Build Settings Window (Ctrl-Shift-B or File->Build Settings)
  * Ensure "RenderTexture" is the in the Build Scenes List and Checked
  * Ensure "Universal Windows Platform" is the selected Platform
  * Click "Build and Run", this will build, deploy and run the Unity App as a Universal Windows Application

## Testing the System

1. The system can be executed on a local network without the need for Internet access to Google servers.
1. On the (Visual Studio Workstation), open a command window with Administrative access
1. Get the IP Address of the workstation
1. Make sure the workstation firewall allows port 8888 access
1. go to the \\ExternalProjects\\WebRTCPeerConnectionServerExe Folder
1. Run the peerconnection_server.exe (this came from the WebRTC core source code)
1. On the (Unity3D Development Workstation), change the IP address to the value (Visual Studio Workstation) address on the running Unity Application
1. Click "Connect" on the Unity3D and XAMLTestApp (this defaults to localhost) to connect to server
1. Click "Connect Peer" to establish a peer session


## Known Issues

* Unity Peer Application only receives video/audio feed from transmitting peer.  Webcam/Mic is activated as required by UWP WebRTC Lib
* The plugin can be optimized further by using shaders to handle the color conversion


## Notes

A brief description of the InterOp in the project is at [Microsoft Real Life Code: Revisiting InterOp with Unity, UWP and DirectX]( https://www.microsoft.com/reallifecode/2017/06/28/revisiting-interop-unity-uwp-directx/)
