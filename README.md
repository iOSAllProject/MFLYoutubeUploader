# MFLYoutubeUploader
I wanted an incredibly simple class for uploading videos to Youtube. If you're like me, and all you want to do is upload a video to YT then YTDL is going to seem monolithic. No need to stress, Youtube uploading is actually incredibly simple.

####Account Setup
First you'll need to get registered with Google in order to make uploads. [Start here](https://console.developers.google.com/project)

(https://cloud.google.com/console#/flows/enableapi?apiid=youtube)

1) Create an Application.

  - If you haven't already registered your application with the Google, then set up an application. The system will guides you through the process of setting up your application

  - Once you've already registered your application with the Google, you'll need to get your Client ID, and Client Secret to provide to the manager.
  
      - Select project from your [console](https://console.developers.google.com/project).
      - Choose APIs & Auth
      - Choose Credentials
      - On the far right, you should see Client ID and Client Secret. Copy these into the corresponding constants in the MFLYoutubeUploader
      
      
2) Integrate the Google Client Library

  - This library is quite large, and may be one of the more complicated steps you have to deal with.
  - Download a read-only copy from [here]() or checkout via SVN
```  
  svn checkout http://google-api-objectivec-client.googlecode.com/svn/trunk/ google-api-objectivec-client-read-only
```

  - If you place the resulting directory next to your project file, you will want to use the following Header Search Paths:
    
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source"
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source/Services/YouTube/Generated"
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source/Utilities"
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source/OAuth2/Touch"
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source/OAuth2"
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source/Objects"
    - "$(SRCROOT)/google-api-objectivec-client-read-only/Source/HTTPFetcher"

3) Manual Loading Indicator, or Automatic Loading Indicator?

  - TBD, there will be a progress callback, but there will also probably be automatic loading indicator management if you choose.
  
  
  
####Thanks
Thank you to [YouTube Direct Lite for iOS](https://github.com/youtube/yt-direct-lite-iOS) for getting me started on this.
