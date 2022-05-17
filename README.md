# Workadventure (Campus Nordhausen)

## Table of contents:
1. Introduction:  
  1.1. Overview:  
  1.2. Goals:  
2. Workadventure for Campus Nordhausen:  
  2.1. Software System  
  2.2. Maps Customization  
  2.3. Public and private map hosting

3. Evaluation (comments and reviews)  
  3.1. Maps validation with public server (github server)  
  3.2. Maps validation with private server  
    - 3.2.1. Configure private server with Virtual Machine  
    - 3.2.2. Maps validation with Virtual Machine  

4. Summary and Conclusion  
  4.1. Summary of results  
  4.2. Lessons learn  
  4.3. Future development  

## 1. Introduction:
### 1.1. Overview:  
Communication has always been one of the fundamental need of human being since the ability to talk and origin of language. Communication methods have also gone a long way from direct conversation, where individuals have to be in the same closed space, to long distance communication through long-waiting writing, to phone call, to sms, emails and voice mails that wait to be checked, to recently direct real-time back and forth chatting and calling with video, which also known as video call. The Internet development in this era has great impact on contributing to improve effectiveness of working, learning and social organizing, which includes distance communincation. Video Meeting (Conference) has been generally taken into account for years as a focused method of distance communication and particularly focused in the situation of Corona Pandemic, where people have to isolate themselves to stay and work at home (home office) most of the time. Here are quick summary of currently popular VC methods.

There are two different current methods to form a Video Conference: 
| Method | Highlight tools | Description |
| - | - | - |
| Technical | Jitsi, Zoom, Big Blue Button | Here switch the participants technically to another session (i.e. another "room"). You can no longer see anything except this room, so you cannot see what is going on outside the room or where a friend has "moved" to. |
| Avatar | Workadventu.re (WA), Wonder.Me (WM), Gather Town (GT) | The participant is shown as an avatar in a digital room and also sees all breakout rooms. Users can move in or out of these rooms by controlling their avatar on the screen. When entering a room, the participant only hears the people in the same room. They can still see who is in other rooms and make decision whether to change rooms or not. This behavior comes closer to our conventional social behavior. |

In comparison between these methods, there are some important properties that help choosing which method between different types of users.
| Properties | Gather Town | ***Workadventure*** | Wonder Me | Big Blue Button | Zoom | Jitsi |
| ---|---|---|---|---|---|---|
| maximum number of users |25 (free of charge)|***60***|1500|tbd|100|50|
| requirement of login/registration|no, except for cumtomized rooms|***no***|no, only moderators must register|no|optional|no|
| password security for meetings|no|***no***|no|yes|yes|yes|
| ability to set up a lobby for admitted attendants before joining|no|***no***|no|no|yes|yes|
| Web browsers-plugin|no|***no***|no|no|yes|yes|
| App|no|***no***|no|no|Win, IOS, Android|Win, IOS, Android|
| Chat in meetings|yes|***no***|yes|yes|yes|yes|
| Breakout rooms|yes|***yes***|yes|yes|yes|no|
| background customize|no|***no***|no|no|yes|yes|
| ability to mute all participants|no|***no***|no|yes|yes|yes|

### 1.2. Goals: 
The goal of this project is a small research of Workadventure, one of the currently popular Video Conference (VC) method, which is known for having features that bring day-life familiar experience to users, to find and show its advantages, disadvantages and using difficulty.
Although Gather Town (GT) is similar to Workadventure (WA), the only upside GT has is Chat in Meeting, which is sometimes unnecessary since it's voice and video communication. WA also has larger number of paticipants. In comparison with Wonder Me, WA has better outlook with custom maps and humanlike Avatar, while Avatar in Wonder Me are only circles moving around in a blank space, which reduce load memory so that it has up to 1500 paricipant but then lack of characteristic to identify individuals, which is an important behavior of human that this project also want to focus on. Hence Workadventure is the choice for this project.

## 2. Workadventure for Campus Nordhausen:
### 2.1. Software System
Following the instruction of Workadventure Documentation, the [Tiled Editor](https://www.mapeditor.org/) software is the basic tool to create a custom map alongside with some different tilesets. WorkAdventure comes with a ["map starter kit"](https://github.com/thecodingmachine/workadventure-map-starter-kit) which contains a good default tileset for building an office and it proposes to use Github static pages as a public web-server which is both free and performant. It also comes with a local webserver for testing purpose and with Typescript support.
A Virtual Machine provided by Thomas Hühn will be used for private hosting server. 
### 2.2. Map Customization
Learning how to create map on Tiled and reading some basic rules for custom maps from [Workadventure Documentation](https://workadventu.re/map-building/) are mandatory.
From that 5 maps with multiple layers that have access to each other are drafted.

The first map is **Campus yard** map. It is planed to have 4 entrances to access to 4 different places which are (2) **Library**, (3) **Mensa**, (4) **Audimax** and (5) a **Seminar**.  
<img src="https://user-images.githubusercontent.com/66717834/167427269-38432496-7f84-46fe-901c-6a51fe8961c5.png" alt="Campus" width="500"/>

With this map, I have 12 layers drafted, which are, from above to below  

***Photo goes here***

As mention in the Documentation, there muss be an above overall object layer named "floorLayer" to represent the Avatar instance of users, where the "override" layer above it normally contains all the roofs of objects that are above our head. For "object", "building" and "ground" layers I use some additional tilesets to decorate. There are some jitsi instances (layers) around the staircase in the middle of the map which connect to a jitsi room by these properties

***Photo goes here***

There are 4 exit points and entry points to the other 4 maps so there should be also 4 pairs of "exitTo..." layer (identified by ) and "startFrom..." layer

### 2.3. Public and private map hosting

## 3. Evaluation:
### 3.1. Maps validation with public server (github server)

### 3.2. Maps validation with private server  
**3.2.1. Configure private server with Virtual Machine**  
**3.2.2. Maps validation with Virtual Machine**  
    

## 4. Summary and Conclusion  
### 4.1. Summary of results

### 4.2. Lessons learn

### 4.3. Future development
