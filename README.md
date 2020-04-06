# Iphone-Zoom-ThroughTD
Quick setup to stream Iphone screen live capture to Zoom, through TouchDesigner, enableling the user to Chroma key the background and created different effect over the captured footage. 
You'll need the following:
IPhone
Spout, we will use SpoutCam. It only runs on Windows.
NDI HX Capture IOS app
Install NDI tools 
TD educational or commercial license. In Jarret's latest post, he mentions that in next week's build, the NDI tools will also be available for non-commercial builds. As for now you'll need commercial.
Zoom
Once you install these tools, how does this work? 
Well, you will use the NDI HX app to capture your iPhone screen and stream it into TouchDesigner. In TD, you'll be able to process this footage and create multiple real-time effects; including chroma-keying the background and replacing it with your own real-time graphics.

This footage comes into TD using the "NDI In" TOP.

For Background Removal, you can use the iPhone camera app. Look for the "Portrait" lighting effects, and choose either: 

StageLight
Stage Light Mono
High Key light Mono
All of these iPhone camera features will remove the background and replace it with either black or white. Once you have this footage in TD, you can apply different TOP effects to clear the background. I added some examples in the TD file I'm sharing, but settings will depend on your facial features, clothing, lighting, etc
Once you have created your new background, you will send it to the "Syphon Spout Out" TOP operator. 

This is where Spout comes into play. Spout is a real-time video sharing framework for Windows,  and has a "virtual camera" feature called "spoutCam". Once Spout is downloaded, open the spoutCam folder to set up the resolution of your camera. ( It should match the aspect ratio of the TOP you are sending to SPOUT, otherwise, the feed will get distorted) 
Once Spout is set up correctly and your footage connected to the Spout OUT Top, go to Zoom. 

In the Zoom interface, once you join or start a meeting, right-click next to the video camera and an option to use "spoutCam" will show pop up. Choose this camera. 

As an overall recap this is the workflow: 

Stream from your phone into TD
Image processing and real-time graphics in TD
Spout it out to Zoom.

I have only tried this with Zoom, but my guess is that spoutCam will work on other video streaming software since the software detects it as another camera input.

You could also use "NDI Virtual Input" instead of Spout to connect to social media. Jarret explains this in his latest post. 
