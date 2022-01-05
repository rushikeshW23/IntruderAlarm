# IntruderAlarm using ESP8266
---------------------------------------------------------------------------------------------

# Project at a glance…
This project is based on IoT(Internet of Things). We have made an intruder alarm using ESP8266 microcontroller, PIR Motion sensor and Buzzer (as important components) etc.

When anybody (human, animal or body emitting infrared radiations) emitting heat waves comes close to our project (installation site). PIR motion  sensor will instantly detect the presence of it and rings a buzzer alarm to notify us about an intrusion. The microcontroller sends a notification on the phone through IFTTT Webhooks (which helps us connect all of our different apps and devices) and also sounds the buzzer when motion is detected.

   <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/projectImage.jpg" alt="img" width="350 px" height="250 px">
<!-- ![alt text]() -->

# Principle

This project based on the priciple that : - Every body emits heat waves and heat waves contain infrared radiations. The more the body emitting heat the more the infrared radiations. Generally the living bodies emit more heat than the raw materials. So the PIR sensor can be used to detect the motion of living bodies. Everything works through the internet so there is no limitation of the distance between the sensor and the phone.

# Hardware required

1. NodMCU ESP8266

 <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/nodemcu.jpeg" alt="img" width="400 px" height="250 px">
 
2. PIR Sensor

 <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/PIR%20sensor.png" alt="img" width="400 px" height="250 px">
 
5. Active Buzzer
 
<!--  <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/buzzer.jpg" alt="img" > -->

6. LED
  
<!--   <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/led.jpg" alt="img" width="300 px" height="250 px" > -->
  
8. Breadboard

<!-- <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/breadboard.jpg" alt="img"> -->

9. Jumper wires

<!--   <img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/Jumper%20wires.jpg" alt="img" width="250 px" height="250 px" > -->
  
# Workflow

<img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/Picture1.png" alt="img" width="500 px" height="450 px" >


•	We have connected the PIR motion sensor to to the digital pin D8 (GPIO 15) of NodeMCU.

•	Whenever the PIR detects motion then the output state of the PIR sensor will change which will be detected by the controller.

•	We have programmed the NodeMCU to make an HTTP GET request to our IFTTT Webhooks app.

•	Whenever the HTTP GET request has been made then it will trigger a notification alert on our mobile phone or the device connected.

# Circuit and Connections

<img src="https://github.com/rushikeshW23/IntruderAlarm/blob/main/Resources/circuit%20diagram.jpeg" alt="img" width="500 px" height="450 px" >

# IFTTT Applet Creation
<ul>
  <li>Download the Andriod app from Play Store.</li>
 
  <li>Create an Account (If you don't have an account)</li>
 </ul>

<ol>
  <li>Click on your profile icon and select the create option</li>
 
  
  <li>Now click on +This</li>
  
  
  <li>Search for "Webhooks" and select it</li>
  
  
  <li>Choose trigger option, "Receive a Web Request"</li>
  
  
  <li>Give a name to your event. In our case, we have used "motion_detected"</li>
  
  
  <li>Now click on +That</li>
  
  
  <li>Now from “choose action service”,</li>
  
  
  <li>Search for notification in the search box and click on the notification icon.</li>
      • Note that you must be installed and logged in to the IFTTT app on your phone for the notifications to work.
  
  
  <li>Choose Simple Notification</li>
  
  
  <li>Type the custom message you want to receive the notification.</li>
  
  
  <li>Click Finish.</li>
</ol>
<b> Obtaining the HTTP GET request URL </b>
  <ol>
  
  <li>Log in to your IFTTT account</li>
  
  
  <li>Click on profile and choose "My Services"</li>
  
  
  <li>Select Webhooks</li>
  
  
  <li>Click on Documentation</li>
 
  
  <li>Now replace "{event}" with your even name in Step 5 of IFTTT Applet creation</li>
 
  
  <li>Now copy the key and paste it into the code</li>
 </ol>

  
  
