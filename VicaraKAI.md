 # __KAI__
* KAI controls the  digital device without any direct contact to device.
* KAI is a gesture based interaction with any bluetooth enabled device.
* KAI can be used while working with keyboard and mouse.
* KAI is compatible with all the applications.
* KAI is wireless gesture based controller.

 # __Software stack__
 * Multiple KAIS can be connected to a single dongle.
 * It uses C#, Python and Node.js for communicating with modules. 
 * Has various components like SDK, Control center, KAI control center.

 ## __SDK__<br>
 * SDK consist of 2 ways communication<br>
    * Process: process uses  standard input/output for communication.<br>
    * WebSocket: 
        When a KAI device is connected it displays that KAI is connected with KAI ID and also detects which hand is connected. 
        If any gesture is performed it displays the type of gesture.
        ```
          type:connected,
          KaiId: 0,
          defaultlefthand: true,
          gesturetype:gesture,
          gestureperformed:Swipe up
        ````

 ## __KAI control center__
* Using kai control center favorite gestures can be paired with the  applications.
* It contains datatypes like gestures data, pyr data, Accelerometer data, Fingerlickr data, Gyroscope data and Magnetometer data.
* Users can adopt there own gestures.

 ## __Control center__
 * Contains modules and can handle events.
 * User gestures are recognized by dongle and sent to SDK for decoding and from SDK it is sent to module to perform action.
 * Control center suggests interaction options based on the software we choose. 

# __JSON Format__
1. __Authentication:__ It sends the module Id and module secret and gives the response type as authentication.

1. __Switch hand:__ It gives the information about type, KAI Id and hand either left or right.

1. __Get KAI Data:__ It gives the Information about Kai Id , type and data type.

1. __Setting Capabilities:__ The datatypes are set to either true or false.

1. __Unknown Data:__ If an request is sent with unknown datatype it displays error.

1. __Sample Authentication:__ If the request is sent before authentication it displays an error message or exception.
 
 