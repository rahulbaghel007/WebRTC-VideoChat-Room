Here, you can understand the working and how to run this project locally. 
# PeerVC Video Chat Application

PeerVC is a WebRTC-based video chat app that establishes direct peer-to-peer video calls between users.

The signaling server powered by Agora facilitates the initial handshake between peers to enable clients to share session descriptions and ICE candidates required for the peer connection. Once established, the video streams are transmitted directly between peer browsers.

## Signaling

The Agora Real-Time Messaging (AgoraRTM) SDK is leveraged for signaling between peers to set up the WebRTC connection.

AgoraRTM provides a secure and low-latency channel for peers to exchange messages for user coordination, joining channels, and client synchronization required for WebRTC handshake.

## Architecture 

The app is built using:

- Vanilla JS on the client-side to handle UI and WebRTC logic
- Agora Web SDK for accessing WebRTC features   
- Node.js and Express server to serve static content
- Websocket connections handle signaling for session establishment

Key components:

- Frontend
  - Client-side WebRTC handling
  - Local stream capture & rendering 
  - Peer event handling
- Signaling Server
  - Powered by Agora SDK Websocket connections
  - Facilitates WebRTC handshake between clients
- App Server
  - Serves static HTML, CSS & JS
  - Hosts the environment

## Running Locally  

Prerequisites:  

Good command on HTML, CSS and JavaScript.

 Clone repo
```
  git clone https://github.com/rahulbaghel007/WebRTC-VideoChat-Room.git

```

 Create account over Agora : 
  - Officail Website--> https://www.agora.io/en/
  - Documentaion --> https://docs.agora.io/en/video-calling/get-started/get-started-sdk?platform=web

 Create the Project over Agora
  - Create a project over Agora with appropiate name and generate the APP_ID which will be used in the project for establshing the Pear-Communication.

 Download Signaling SDK for Web to use all the pre-define functionlity of Agora RTM
  - https://docs.agora.io/en/sdks?platform=web

 Extention for Auto Running server file 
  - Whenever there is change the codebase and as you save, the automatically the server reload and will show all the changes you made on the webpage.

 App runs on port 5500
  - http://localhost:5500 

The signaling server runs independently via Agora. Developers can signup for free trial keys.  

## Client-Side Workflow   

The client-side app handles:   

- Local media capture
- Rendering local video stream  
- Creating peer connection
- Managing WebRTC connections
- Streaming video between peers 
- UI event handling  

### WebRTC Interactions

The WebRTC APIs used include:  

- MediaDevices.getUserMedia() 
- RTCPeerConnection()    
- RTCDataChannels  
- addStream()  
- createOffer() / createAnswer()  

Session connectivity is handled entirely client-side leveraging the Agora SDK for signaling.  

## Future Features   

Enhancements under consideration:

- Text chat
- Screen sharing capability  
- Support for N peer connections  
- Improved mobile experience
- User account management
- Video recording  

## Additional ideas or feedback welcome! 
Developer email id = codeforbest@gmail.com
Personal email id = rahulbaghel5720@gmail.com
