# Workadventure (Campus Nordhausen)
## Introduction:
### 1. Overview:
Communication has always been one of the fundamental need of human being since the ability to talk and origin of language. Communication methods have also gone a long way from direct conversation, where individuals have to be in the same closed space, to long distance communication through long-waiting writing, to phone call, to sms, emails and voice mails that wait to be checked, to recently direct real-time back and forth chatting and calling with video, which also known as video call. The Internet development in the era has great impact on contributing to improve effectiveness of working, learning and social organizing, which includes distance communincation. Video Meeting (Conference) has been generally taken into account for years as a focused method of distance communication and particularly focused in the situation of Corona Pandemic, where people have to isolate themselves to stay and work at home (home office) most of the time. This project is a small research for one of the currently popular Video Conference (VC) method which is known for having features that bring day-life familiar experience to users and to find and show its advantages, disadvantages and using difficulty as a reference for anyone who has interest in it.

### 2. Goals: 
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
* Tiled editor
* "map starter kit" provided by workadventu.re that contains default tileset for building maps
* additional tilesets on google per topics

For this project and following the instruction, Tiled editor along with 'map starter kit' provided by WA are tools for creating custom maps. However it is not enough and I also have to find some other tilesets on google which contain my desire tiles. [^2]
[^2]:[WA Tutorial](https://workadventu.re/map-building/)
* a web-server: Github static page
* Node.js

These 2 tools are used for launching and testing custom map.

* Windows Subsystem For Linux: Ubuntu
* Docker and Docker-Compose
* Sample Repositories for WA

These tools are for hosting and launching private server.
### 2. Related work:
#### 1. Custom map:
After watching some basic Youtube videos about creating maps on Tiled, I have finished drafting out 5 maps that can be linked to each other. These maps are:
- Campus yard (49x46)
<img src="https://user-images.githubusercontent.com/66717834/149056247-c36a3d8f-ee86-4c53-82f3-2037fcc0b020.png" alt="Campus">

- Campus Library (32x32)
<img src="https://user-images.githubusercontent.com/66717834/149056712-97879e8e-86f9-4455-a7a2-e1c78a0920bf.png" alt="Bibo">

- Campus Mensa (32x32)
<img src="https://user-images.githubusercontent.com/66717834/149056712-97879e8e-86f9-4455-a7a2-e1c78a0920bf.png" alt="Bibo">

- Campus Audimax (32x32)
<img src="https://user-images.githubusercontent.com/66717834/149056712-97879e8e-86f9-4455-a7a2-e1c78a0920bf.png" alt="Bibo">

- Campus Seminar (32x32)
<img src="https://user-images.githubusercontent.com/66717834/149056712-97879e8e-86f9-4455-a7a2-e1c78a0920bf.png" alt="Bibo">


#### 1. Workadventure on localhost and on play.workadventu.re server:
1. Experience some example servers and experiment demo map on workadventu.re
2. Follow WA instruction:
    1. Get a general understanding of some basic terminologies
    2. Clone Github "map starter kit" to personal repository
3. Learn about Tiled editor and customize Map on it by following WA Instruction:
    1. Get used to Tiled Editor
    2. Create general Campus Map with at least 4 locations/buildings per choice
    3. Create 4 particular Maps for 4 different locations/buildings mentioned above with Jitsi URL for Video Conferencing
    4. Each map should be formed by multiple layers, which must include at least Objectlayer (named floorLayer), exit layers where links leading to other maps are assigned and     start layers where characters should be spawning.
4. Perform test on localhost
5. Push pository to github and perform test on WA server.

#### 2. Workadventure self-hosted server:
1. Research for how to host a server from some instructions on the Internet from devnope, RC3 and thecodingmachine
2. Get a general understanding of Windows Subsystem For Linux, since most tutorials are based on Linux OS.
3. Get a general understanding of Debian/Ubuntu and Linux OS command syntax.
4. Connect to Virtual Machine (VM) used for hosting server.
5. Get a general understanding of how to install software components in VM for server hosting: Docker, docker-compose, Ansible, etc.
6. Follow instruction from sample repo to clone into VM and config server setting.
7. Config access ability to customers via ssh keys.
8. Perform test, troubleshoot and launch.

## Consclusion:
### 1. Link to WA provided server:
* play.workadventu.re: https://play.workadventu.re/_/global/ginhavana.github.io/Workadventure_Campus_NDH/Workadventure-Campus-NDH-WA-Server/Campus_NDH.json

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
