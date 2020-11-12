# 1to1 RTC: A Sample Web App using Vue.js (JS Framework) and EnableX Web Toolkit

The Sample Web App demonstrates the use of APIs for EnableX platform to develop basic 1to1 RTC (Real Time Communication) Application. The main motivation behind this application is to demonstrate usage of APIs and allow developers to ramp up on app by hosting on their own devices instead of directly using servers.

RTC Applications hosted on EnableX platform run natively on supported set of web browsers without any additional plugin downloads.

This basic 1to1 RTC Application is developed using HTML, CSS, Bootstrap, JavaScript, jQuery, Vue.js and EnxRtc (The EnableX Web Toolkit).

> The details of the supported set of web browsers can be found here:
> https://developer.enablex.io/video/browser-compatibility-of-enablex-video/


## 1. Important!

When developing a Client Application with EnxRtc.js, make sure to include the updated EnxRtc.js polyfills from https://developer.enablex.io/video-api/client-api/web-toolkit/ for RTCPeerConnection and getUserMedia. Otherwise your application will not work in web browsers.


## 2. Trial

Sign up for a free trial https://portal.enablex.io/cpaas/trial-sign-up/ or try our multiparty video chat https://try.enablex.io/


## 3. Installation

### 3.1 Pre-Requisites

#### 3.1.1 App Id and App Key

* Register with EnableX [https://portal.enablex.io/cpaas/trial-sign-up/] 
* Create your Application
* Get your App ID and App Key
* Clone this repository `git clone https://github.com/EnableX/One-to-One-Video-Calling-VueJS-Open-Source-Application.git --recursive`


#### 3.1.2 Sample App Server

* You need to have an App server. Get any of the Repositiory listed below to setup your App Server:
  * Laravel [https://github.com/EnableX/WebRTC-Open-Source-One-To-One-Video-Chat-Application-in-Laravel]
  * PHP     [https://github.com/EnableX/One-to-One-Video-Calling-Open-Source-PHP-Application]
  * Nodejs  [https://github.com/EnableX/One-to-One-Video-Chat-Sample-Web-Application]
  * Python  [https://github.com/EnableX/WebRTC-Python-Open-Source-Application-for-1-to-1-video-chat]
  
* Clone Repository of your choice & follow the steps further
* You need to use App ID and App Key to run this Service.
* Your Vuejs Client End Point needs to connect to this Service to create Virtual Room.
* Follow README file of the cloned Repository to setup the Service.

#### 3.1.3 SSL Certificates

The Application needs to run on https. So, you need to use a valid SSL Certificate for your Domain and point your application to use them. 

However you may use self-signed Certificate to run this application locally. There are many Web Sites to get a Self-Signed Certificate generated for you, Google it. Few among them are:

* https://letsencrypt.org/
* https://www.sslchecker.com/csr/self_signed
* https://www.akadia.com/services/ssh_test_certificate.html  

As you have Certificate or created a Self-Signed Certificate, create a directory "certs" under your Sample Web App Directory. Copy your Certificate files (.key and .crt files)  to this directory.

### 3.2 Test

* Open a browser and go to [https://yourdomain.com:4443/path-to-sample-app](https://yourdomain.com:4443/path-to-sample-app). The browser should load the App. 
* Allow access to Camera and Mic as and when prompted to start your first RTC Call through EnableX
* You need to Room ID to join. We have added a "Create Room" link below the login form. Click it to get a Room-Id prefilled in the form. 
* You can share the Room-ID with anyone to join your Conference.

## 4. Server API

EnableX Server API is a Rest API service meant to be called from Partners' Application Server to provision video enabled
meeting rooms. API Access is given to each Application through the assigned App ID and App Key. So, the App ID and App Key
are to be used as Username and Password respectively to pass as HTTP Basic Authentication header to access Server API.

For this application, the following Server API calls are used:
* https://developer.enablex.io/video-api/server-api/rooms-route/#create-room - To create room to carry out a video session
* https://developer.enablex.io/video-api/server-api/rooms-route/#create-token - To create Token for the given Room to join a session

To know more about Server API, go to:
https://developer.enablex.io/video-api/server-api/


## 5. Client API

Client End Point Application uses Web Toolkit EnxRtc.js to communicate with EnableX Servers to initiate and manage RTC Communications.

To know more about Client API, go to:
https://developer.enablex.io/video-api/client-api/
