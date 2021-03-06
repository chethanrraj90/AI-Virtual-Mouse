# AI-Virtual-Mouse

## Abstract

Even today, many people still find interacting with computers and hardware to be an unpleasant 
experience, despite the development of input devices over decades. Computers and hardware should be tailored to our 
natural modes of communication: Body language and speech. Intelligent machines that can work alongside computers 
are now being developed, allowing for friendlier Human-Computer Interaction (HCI). Our proposed project, on the 
other hand, intends a hand gesture-based system that allows users to control desktop mouse movements. To detect hand 
gesture movements, our system makes use of a desktop webcam. The goal is to control mouse cursor functions with a 
simple camera rather than a traditional or standard mouse device. Using only a camera, the Virtual Mouse provides an 
infrastructure between the user and the machine. It enables the user to interact with a machine without the need for any 
mechanical or physical devices, and even allows to control mouse functions.
 
  ## Problem Definition
     
To design virtual mouse which detects hand gestures patterns instead of physical mouse. The camera is positioned such that it recognizes the moment of finger tips and performs the operations of mouse. The utilization of virtual mouse appears in space saving situations or in movement situation.
  
   ## Objectives

- The goal is to manage computers and other devices with    gestures rather than pointing and clicking a mouse or touching a display directly.
- The system will allow the user to navigate the computer cursor using their hand gestures and left click and scrolling will be performed using different hand gestures.
- To reduce the cost of hardware.


## Implimentation
    
The project is divided into 2 sub-programs :- 

1.Hand Tracking Module.
The framework used is Mediapipe developed by google.
It uses two main models ,
- Palm detection 
- Hand landmarks 

2.AI Virtual Mouse Module.

After the palm detection over the whole image our subsequent hand landmark model performs precise key point localization of 21 3D hand-knuckle coordinates inside the detected hand regions via regression, that is direct coordinate prediction.
The model learns a consistent internal hand pose representation and is robust even to partially visible hands and self-occlusions.
 
- Find hand Landmarks.
- Check which fingers are up.
- Only Index finger: Moving Mode.
- Convert Coordinates.
- Smoothen Values.
- Move Mouse.
- Both Index and middle fingers are up : Left click Mode.
- Find distance between fingers.
- Click mouse if distance short.
- Both Index and thumb up: Scroll
- All five fingers are up : right click mode
- Frame rate.
- Display.

## Guide

  1. Move curser---------------Index Finger(up)
  2. Left click-----------------Index and Middle finger(up and closer)
  3. Right click---------------all 5 fingers(up)
  4. Scrolling---------------Thumb and Index finger(up and closer)
