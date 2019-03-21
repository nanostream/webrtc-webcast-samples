# webrtc-webcast-samples

(c) 2019 nanocosmos gmbh

## How to use WebRTC.live with nanoStream Cloud?

It is very simple to test and use nanoStream WebRTC.live as your live encoder to nanoStream Cloud with integrated nanoStream H5Live Player. You need a camera connected to your computer or built-in on your device, and a WebRTC-compatible browser. We recommend using Google Chrome.

### Create your own nanoStream Cloud account

To stream directly to nanoStream Cloud you will need to register at [bintu.live](https://bintu.nanocosmos.de/) . 

>Bintu.live is the rest API and stream management tool included in nanoStream Cloud. You can find the step-by-step guide to register by [clicking here.](http://docs.nanocosmos.de/docs/cloud/cloud_getting_started)
>
>Once registered, you can create new URLs by calling the bintu API with a valid API key.

-----

## nanoStream WebRTC Browser API

The nanoStream WebRTC Browser API is based on a Javascript API connected to the nanoStream WebRTC Server. It can be used for creating your own live video broadcast web page for plugin-free live streaming with WebRTC.




### Hosting Requirements

You will need the following requirements to be fulfilled in order to host a WebRTC driven website on your own infrastructure:

- HTTPS: **WebRTC client web pages need to be hosted via HTTPS** for accessing media devices within the browser and for connecting to the server component. Therefore you will need a valid SSL certificate.
- Supported browsers: As of 2018, Chrome, Firefox, Edge and Safari are supported. For mobile platforms we recommend Safari on iOS (min iOS11) and Chrome for Android. 



## Broadcast Sample

The following sample shows how to initiate a broadcast (one-to-many stream) from a WebRTC enabled HTML5 browser.

The stream is sent to an `RTMP` ingest point which you can get from our bintu.live API.
Playback can be done with nanoStream H5Live Player.

Be sure to attach a video device (webcam) to your computer.

You also find a full running [sample at codepen](https://codepen.io/nanocosmos-ol/pen/Xybadx)



###  Setup The User Interface & Embed The Library 

Within your HTML:
```xml
<body>
  <!-- videoelement to preview your video device (camera) -->
  <video id="video-local" autoplay playsinline style="width:800;height:600"></video>

  <!-- buttons for start/stop of broadcast -->
  <button id="btn-startbroadcast">broadcast</button>
  <button id="btn-stopbroadcast">stop broadcast</button>
    
  <!-- embed the nanoStream WebRTC.live library -->
  <!-- replace "<version>" with the version contained in your package -->
  <script src="./js/api/webrtc/nano.webrtc.<version>.min.js"></script>
</body>
```
