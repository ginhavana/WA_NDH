# Workadventure (Campus Nordhausen)

## Table of contents:
1. Introduction:
    1.1. Overview:
    1.2. Goals:
    1.3. 
2. Main part:
    2.1. Software System
    2.2. Maps Customization
    2.3. Maps validation with workadventure server
    2.4. Configure private server with Virtual Machine
    2.5. Maps validation with private server
3. Conclusion












## 1. Introduction:
### 1.1. Overview:
Communication has always been one of the fundamental need of human being since the ability to talk and origin of language. Communication methods have also gone a long way from direct conversation, where individuals have to be in the same closed space, to long distance communication through long-waiting writing, to phone call, to sms, emails and voice mails that wait to be checked, to recently direct real-time back and forth chatting and calling with video, which also known as video call. The Internet development in the era has great impact on contributing to improve effectiveness of working, learning and social organizing, which includes distance communincation. Video Meeting (Conference) has been generally taken into account for years as a focused method of distance communication and particularly focused in the situation of Corona Pandemic, where people have to isolate themselves to stay and work at home (home office) most of the time. This project is a small research for one of the currently popular Video Conference (VC) method which is known for having features that bring day-life familiar experience to users and to find and show its advantages, disadvantages and using difficulty as a reference for anyone who has interest in it.

### 1.2. Goals: 
1. Quick summary of currently popular VC methods and reason why Workadventure is choosen.
2. Workadventure experience:
    1. Experiencing creating a self-made map. The choosen inspiration is a map of Campus Nordhausen with at least 4 particular locations with potential for further development as a substitute learning method.
    2. Experiencing self-made map on workadventu.re provided server.
    3. Experiencing hosting a local server for permitted individuals as private server.

## Design Consideration[^1]
There are two different current methods to form a Video Conference: 
| Method | Highlight tools | Description |
| - | - | - |
| Technical | Jitsi, Zoom, Big Blue Button | Here switch the participants technically to another session (i.e. another "room"). You can no longer see anything except this room, so you cannot see what is going on outside the room or where a friend has "moved" to. |
| Avatar | Workadventu.re (WA), Wonder.Me (WM), Gather Town (GT) | The participant is shown as an avatar in a digital room and also sees all breakout rooms. Users can move in or out of these rooms by controlling their avatar on the screen. When entering a room, the participant only hears the people in the same room. They can still see who is in other rooms and make decision whether to change rooms or not. This behavior comes closer to our conventional social behavior. |

[^1]: [Video-Conferencing tools - Platform für Digitale Initiativen](https://digitaleinitiativen.at/video-conferencing-tools/)

Since one purpose of developing and improving technology day by day is bringing the experience closer and friendlier to users, it is safe to say Technical method are not main consideration of this research. Two tools (Gather Town and Workadventure) develope the conventional behavior further, in which participants can also hear and see (via video) each other when their avatars approach in a certain radius. Therefore these two tools will be particularly taken into account.

However for general point of view, in the next part, Technical method will still be used as references to compare properties between multiple methods.

### 1. important properties as criteria for the choice of tools:[^1]
* Supported number of participants: up to 25, in exceptional cases up to 100
* Preferably using without login (i.e. registration)
* possible securing of a meeting with a password
* Optional waiting rooms for participants
* GDPR compliance
* Availability of plugins (Chrome) or apps
* integrated chat
* the possibility of setting up breakout rooms (group rooms for teamwork)
* the possibility of adding a virtual background to your own camera image
* the possibility for the moderator to mute all participants

### 2. Comparison:
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

Although Gather Town is similar to Workadventure, the only upside GT has is Chat in Meeting, which is sometimes unnecessary since it's voice and video communication. WA also has larger number of paticipants. In comparison with Wonder Me, WA has better outlook with custom maps and humanlike Avatar, while Avatar in Wonder Me are only circles moving around in a blank space, which reduce load memory so that it has up to 1500 paricipant but then lack of characteristic to identify individuals, which is an important behavior of human that this project also want to focus on. Hence Workadventure is the choice for this project.

## Instruction:
### 1. Software systems:
* Github repository for WA server test: https://github.com/ginhavana/workadventure/tree/gh-pages
* Github repository for own server host: https://github.com/ginhavana/WA_NDH
* Tiled editor
* "map starter kit" provided by workadventu.re that contains default tileset for building maps
* additional tilesets on google per topics

For this project and following the instruction, Tiled editor along with 'map starter kit' provided by WA are tools for creating custom maps. However it is not enough and I also have to find some other tilesets on google which contain my desire tiles. [^2]
[^2]:[WA Tutorial](https://workadventu.re/map-building/)
* a web-server: Github static page
* Node.js
* Basic knowledge for HTML and Javascript

These 2 tools are used for launching and testing custom map.

* Windows Subsystem For Linux: Ubuntu
* Docker and Docker-Compose
* Sample Repositories for WA

These tools are for hosting and launching private server.
### 2. Related work:
#### 1. Custom map:
After watching some basic Youtube videos about creating maps on Tiled, I have finished drafting out 5 maps that can be linked to each other. These maps are:
1. Campus yard (49x46)  
<img src="https://user-images.githubusercontent.com/66717834/149632252-35938672-200f-4d63-bde2-a31b8d696036.png" alt="Campus" width="800px">
2. Campus Library (32x32)  
<img src="https://user-images.githubusercontent.com/66717834/149632343-f0965359-d4ea-454c-9613-fa6b20df2ab8.png" alt="Bibo" width="600px">
3. Campus Mensa (39x35)  
<img src="(https://user-images.githubusercontent.com/66717834/149632353-3b4ae50c-f5a4-4516-aa05-7bce80da8545.png" alt="Mensa" width="600px">
4. Campus Audimax (40x25)
<img src="https://user-images.githubusercontent.com/66717834/149632366-4331da9f-16a3-4658-9685-16b138a182b2.png" alt="Audimax" width="600px">
5. Campus Seminar (31x25)  
<img src="https://user-images.githubusercontent.com/66717834/149632357-28e3a760-425e-4c76-af00-c02dc34abbb1.png" alt="Seminar" width="600px">

- Detail information following the tutorials:
  * There is always 'floorLayer' above every other layer for each maps to display 'characters' or 'avatars'.
  * If there is a layer above 'floorLayer', it is named 'override' and only contains objectives like doors ceiling or objectives ceilings.
  * Every maps, or 'rooms' will have serveral jitsi areas, or instances, embed with jitsi URL for different video conferences. For this purpose this specific tile <img src="https://user-images.githubusercontent.com/66717834/149628894-2a4162dd-fa1d-41e1-88a5-d6fd442d5dea.png" alt="jitsi"> is used with properties 'jitsiURL = meet.jit.si' and 'jitsiRoom = <room name>'
  * There are always at least one exit point to other maps and one 'start' aka. entry point from other maps.
  * For the general Campus Yard map, there is one specific entry area for first time loading.
  * There is always a 'collide' layer below every other layer to make that position uncrossable, e.g. walls, tables, hard objectives, etc. For this purpose this specific tile ![collide](https://user-images.githubusercontent.com/66717834/149629094-2a01ab10-fb26-4257-8052-20db3b2275ef.png) is used to set property 'collides = true'.

  * Example:
    <img src="https://user-images.githubusercontent.com/66717834/149627746-2d406869-5a54-4872-9a98-a9427e54b00f.png" alt="Properties_campus" width="350px">
    
#### 2. Workadventure on localhost and on play.workadventu.re server:
1. Testing on WA server:
After finishing customizing maps, all maps and related files will be uploaded to a Github repository for storing. Following the instruction provided by WA, their Github repo for map starter kit is cloned and all maps and related file are uploaded to 'gh-page' branch. Since the start map is not map.js as provided in WA repo, there must be a small adjustment in **index.html** file
    
| Line | Original code | Replace code |
| - | - | - |
| 21 | const url = 'https://play.workadventu.re/_/${instanceId}/${host}${path}map.json' | const url = 'https://play.workadventu.re/_/${instanceId}/${host}${path}Campus_NDH.json'; |
| 26 | const mapUrl = window.location.protocol+'//'+window.location.host+path+'map.json'; | const mapUrl = window.location.protocol+'//'+window.location.host+path+'Campus_NDH.json'; |
   
<img src="https://user-images.githubusercontent.com/66717834/149631636-43492e14-bbed-4036-a1ce-5d141a41908c.png" alt="index" width="700px"> 

Then go to **Setting** in the tools tab, go to **Pages** and change source from `root` to `docs` and press **Save**. There is a notice direct to the test web UI which has form **<username>.github.io.<repo-name>**.  
<img src="https://user-images.githubusercontent.com/66717834/149631719-99989069-91a3-453a-9e6d-961c7b714070.png" alt="githubtut" width="500px">
    
The web UI looks something like this  
<img src="https://user-images.githubusercontent.com/66717834/149631915-8623b31b-2ad1-41a6-a364-867977ad1df0.png" alt="testui" width="500px">

After clicking the link, it's time to explore!
2. Testing on local host:
Can perform as above, but instead of using github as webpage to launch the map, this time the map is hosted right on personal computer. Simply by downloading Node.js, redirect commandline to the directory that stores the maps and run `npm install` and `npm run start`, a web browser will be opened and look something like this
<img src="https://user-images.githubusercontent.com/66717834/149632688-4aeac996-3057-40f2-9655-b56ad7086d62.png" alt="local" width="800px">

#### 3. Workadventure hosted on a virtual machine (private self-host): Editing

## Consclusion: (Editing)
### 1. Link to WA provided server:
* 

### 2. Product: 
* Require SSH Public Key from customers to allow access.
* After gaining access, WA selfhosted server on VM via "sudo ssh root@109.73.30.34 -p 22010 -i id_workadventureVM -L  80:127.0.0.1:80"
* Browse to http://play.workadventure.localhost/_/global/maps.workadventure.localhost/ndh/Campus_NDH.json

### 3. Difficulties and problems during work:
1. Maps are formed by several layers, thus sometimes they don't work correctly and need to be rechecked few times.
2. Due to unfamilarity with Linux OS at first and VM, it required large amount of unnecessary deleting and recreating files and repos.
3. Finding /etc/host in personal OS
4. Required large amount of test to find working port, which should be default 8080

### 4. Comparison between the result server and expectation:
* The selfhosted WA server works properly. All functions have been tested.
* The selfhosted WA server matches expectation.

### 5. Conclusion about adventages and disadventages of WA:
1. Advantages:
* Listed advantages from Comparison part
* Avatar Method is game-liked with characters movement, which means there is flexibility between conversations. Participants can choose and switch between different conversations or conferences in the same screen, thus reduce unnecessary tabs and reconnections, since technically all participants from different conversations are online at the same time, which will be determined by having their Avatar appear or not.
* Large number of participants permitted, up to 60
* Custom maps are compatible and servers can be free-charge self-hosted via VM.
* Other communicating methods e.g. Jitsi is attachable to create large area of Meeting, in compare to given small private circle around characters

2. Disadvantages:
* Listed disadvantages from Comparison part
* he UI lacks of complex configuration choices.
* Chat is not included in Meeting or between individuals, there is only 1 general chat.

### 6. Prognosis and expectation of further development
In the past 2 years within the pandemic time, Video Conferencing has proven its promising ability to support human life. Workadventure, as 1 example method, delivers not only so, but also ensures maintaining human behavior of direct through indirect/distance contact. It is expected to be improved further in security and capacity yet still maintaining low memory cost for hosting discrete servers.
