# videoStreaming
Streaming Video with RTSP and RTP
Classes

There are 4 classes in src folder.

Client
This class implements the client and the user interface which you use to send RTSP commands and which is used to display the video. Below is what the interface looks like. You will need to implement the actions that are taken when the buttons are pressed.
Server
This class implements the server which responds to the RTSP requests and streams back the video. The RTSP interaction is already implemented and the server calls routines in the RTPpacket class to packetize the video data. You do not need to modify this class.
RTPpacket
This class is used to handle the RTP packets. It has separate routines for handling the received packets at the client side which is given and you do not need to modify it (but this is valid for the basic part, not for the Additional Exercises). You will need to complete the first constructor of this class to implement RTP-packetization of the video data. The second constructor is used by the client to de-packetize the data. You do not need to modify that.
VideoStream
This class is used to read video data from the file on disk. You do not need to modify this class.
Running the Code

After completing the code, you can run it as follows.

First, start the server with the command

        java Server server_port
where server_port is the port your server listens to for incoming RTSP connections. The standard RTSP port is 554, but you will need to choose a port number greater than 1024.

Then, start the client with the command

        java Client server_name server_port video_file
where server_host is the name of the machine where the server is running, server_port is the port the server is listening on, and video_file is the name of the file you want to request (we have provided one example file movie.Mjpeg). The file format is described in the Appendix.

## Describe stream feature:
You need to press Setup button then you can use Describe Stream Button.
