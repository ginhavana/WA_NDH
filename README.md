# Workadventure (Campus Nordhausen)

## Table of contents:
1. Introduction:  
  1.1. Overview:  
  1.2. Goals:  
2. Workadventure for Campus Nordhausen:  
  2.1. Software System  
  2.2. Maps Customization  
    - 2.2.1. Campus map
    - 2.2.2. Library map
    - 2.2.3. Mensa map
    - 2.2.4. Audimax map
    - 2.2.5. Seminar map  
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
A Virtual Machine provided by Thomas Hühn will be used for private hosting server. For testing custom maps, it is required to have Windows Subsystem For Linux enabled and Ubuntu installed. It is also recommended to have basic knowledge about HTML and Javascript since maps are .json files, Linux commandlines and usage of Docker and Docker-compose
### 2.2. Map Customization
Learning how to create map on Tiled and reading some basic rules for custom maps from [Workadventure Documentation](https://workadventu.re/map-building/) are mandatory.
From that 5 maps with multiple layers that have access to each other are drafted.

#### 2.2.1.
The first map is **Campus yard** map. It is planed to have 4 entrances to access to 4 different places which are (2) **Library**, (3) **Mensa**, (4) **Audimax** and (5) a **Seminar**.  
<img src="https://user-images.githubusercontent.com/66717834/167427269-38432496-7f84-46fe-901c-6a51fe8961c5.png" alt="Campus" width="500">

With this map, I have 12 layers drafted, which are, from above to below  

<img src="https://user-images.githubusercontent.com/66717834/170034123-110b7c08-f9f6-4a85-9819-d825aedeb520.png" alt="Campus-Layers">

As mention in the Documentation, there muss be an above overall object layer named "floorLayer" to represent the Avatar instance of users, where the "override" layer above it normally contains all the roofs of objects that are above our head. For "object", "building" and "ground" layers I use some additional tilesets to decorate. There are some jitsi instances (layers) (identified by ![jitsi-Instance](https://user-images.githubusercontent.com/66717834/170035680-7e3a76b2-1825-459a-9897-f112e7725f22.png)) around the staircase in the middle of the map which connect to a jitsi room by these properties

<img src="https://user-images.githubusercontent.com/66717834/170034538-ef9e0db5-80ea-420d-a925-80f773354da7.png" alt="Campus-jitsi">

|Properties|Description|
|-|-|
|jitsiRoom|(name of jitsi room)|
|jitsiUrl|meet.jit.si|

There are also 4 exit points and entry points to the other 4 maps so there should be also 4 pairs of "exitTo..." layer (identified by <img src="https://user-images.githubusercontent.com/66717834/170036288-bb1f3c24-c3a4-4d05-95e1-beb3b3a48dc4.png" alt="exit-Instance" width="40px">) which has property to redirect to other maps

<img src="https://user-images.githubusercontent.com/66717834/170037432-346c80aa-f987-4f80-a73c-f209ea6a8c0e.png" alt="exitUrl">

|Properties|Description|
|-|-|
|exitUrl|(path to .json file)|

and "startFrom..." layer (identified by <img src="https://user-images.githubusercontent.com/66717834/170036377-1cca3189-afe9-4248-85e5-c3a82226b86c.png" alt="start-Instance" width="40px">) which initializes users' Avatar when they return from other maps

<img src="https://user-images.githubusercontent.com/66717834/170038776-605dc8d9-3a6c-46f4-a97d-4e4dc6c45acf.png" alt="startLayer">

|Properties|Description|
|-|-|
|startLayer|Boolean value "checked"|

The "start" layer beneath almost every layers is used for initializing users' Avatar the first time they load the program. It is identified by <img src="https://user-images.githubusercontent.com/66717834/170040029-ebedbece-2a94-4c89-a242-196bfa232774.png" alt="start" width="40px">
The "collide" layer at the bottom is used for representing all unpassable obstacles such as hard objects or boulders. It is identified by <img src="https://user-images.githubusercontent.com/66717834/170040875-95ff83cf-5d59-4156-be02-15b6ac7b3137.png" alt="collide-Instance" width="40px">
The start, exit, collide and Jitsi instances are similar among all maps.

#### 2.2.2. Library map
The second map, whose entrance is at the bottom of Campus map, is **Library** map

<img src="https://user-images.githubusercontent.com/66717834/171138699-dbb3a062-5747-445d-ad4e-a76d9de443be.png" alt="Library" width="500">

This map contains a locker room section below the entry point, a reception section above the entry point, a small toilet, some shelves along the hall way and a study section in the bottom of the map.
There are 3 separated Jitsi instances for 3 tables in reception section and 3 Jitsi instances for 3 tables in the study section. All the furnitures and wall (black tiles) are designed with collide instances.

#### 2.2.3. Mensa map
The third map, whose entrance is at the top left of Campus map, is **Mensa** map

<img src="https://user-images.githubusercontent.com/66717834/171282241-86ab3acc-6aeb-445e-bbbf-9054673320f2.png" alt="Mensa" width="500">

This map contains a lot of small tables, for each a corresponding Jitsi instance is given.

#### 2.2.4. Audimax map
The forth map, whose entrance is next to Mensa entrance, is **Audimax** map

<img src="https://user-images.githubusercontent.com/66717834/171282241-86ab3acc-6aeb-445e-bbbf-9054673320f2.png" alt="Audimax" width="500">

This whole map has the same Jitsi instance because it is required that all users in the room listen to the moderator on the stage section.

#### 2.2.5. Seminar map
The third map, whose entrance is at the top right of Campus map, is **Seminar** map

<img src="https://user-images.githubusercontent.com/66717834/171282764-abfb2b33-58df-4943-a054-2d7caac04819.png" alt="Seminar" width="500">

The Seminar map is basically a smaller Audimax.

### 2.3. Public and private map hosting



## 3. Evaluation:
### 3.1. Maps validation with public server (github server)

### 3.2. Maps validation with private server  
#### 3.2.1. Configure private server with Virtual Machine**  
#### 3.2.2. Maps validation with Virtual Machine**  

## 4. Summary and Conclusion  
### 4.1. Summary of results

### 4.2. Lessons learn

### 4.3. Future development
