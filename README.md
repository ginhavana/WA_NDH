# Workadventure (Campus Nordhausen)
## Introduction:
### 1. Overview:
The Internet development has greatly affected many aspects in everyday life, one of these aspect is distance communication, which e.g. improving effectiveness of working, learning and social organizing. Video Meeting (Conference) has been generally taken into account for years as a method of distance communication and particularly focused in the situation of Corona Pandemic, where people have to stay and work at home most of the time.

### 2. Goals: 
Launch a local server with a self-made map of Campus Nordhausen (with at least 4 particular locations) with the help of Workadventure (WA) tool kit and test its functionalities.
Each locations is a video conferencing room where users can join in and perceive other attendants. Furthermore, individuals should have the ability to have their own small circle in which they share private conversation directly.

## Design Consideration
### 1. important properties as criteria for the choice of tools:
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

### 2. Comparison and reason of choosing WA over Gather Town (GT):
There are two different methods to form a Video Conference: 
* Technical (Jitsi, Zoom, Big Blue Button): Here switch the participants technically to another session (i.e. another "room"). You can no longer see anything except this room, so you cannot see what is going on outside the room or where a friend has "moved" to.

* Avatar (Workadventu.re, Wonder.Me, Gather Town): The participant is shown as an avatar in a digital room and also sees all breakout rooms. Users can move in or out of these rooms by controlling their avatar on the screen. When entering a room, the participant only hears the people in the same room. They can still see who is in other rooms and make decision whether to change rooms or not. This behavior comes closer to our conventional social behavior.

Two tools (Gather Town and Workadventure) develope this behavior further, in which participants can only hear and see (via video) each other when their avatars approach in a certain radius. Therefore these two tools will be particularly taken into account.

Properties|Gather Town|Workadventure|Wonder Me|Big Blue Button|Zoom|Jitsi
---|---|---|---|---|---|---
maximum number of users|25 (free of charge)|60|1500|tbd|100|50
requirement of login/registration|no, except for cumtomized rooms|no|no, only moderators must register|no|optional|no
password security for meetings|no|no|no|yes|yes|yes
ability to set up a lobby for admitted attendants before joining|no|no|no|no|yes|yes
Web browsers-plugin|no|no|no|no|yes|yes
App|no|no|no|no|Win, IOS, Android|Win, IOS, Android
Chat in meetings|yes|no|yes|yes|yes|yes
Breakout rooms|yes|yes|yes|yes|yes|no
background customize|no|no|no|no|yes|yes
ability to mute all participants|no|no|no|yes|yes|yes

Although Gather Town is similar to Workadventure, the only upside GT has is Chat in Meeting, which is sometime unnecessary since it's voice and video communication. WA also has larger number of paticipants. In comparison with Wonder Me, WA has better outlook with custom maps and humanlike Avatar, while Avatar in Wonder Me are only circles moving around in a blank space, which reduce load memory so that it has up to 1500 paricipant but then lack of characteristic to identify individuals, which is an important behavior of human that this project also want to focus on. Hence Workadventure is the choice for this project.

## Related work:
### 1. Software systems:
* Tiled editor
* "map starter kit" provided by workadventu.re that contains default tileset for building maps
* a web-server: Github static page
* Node.js
* Windows Subsystem For Linux
* Ubuntu/Debian
* Docker and Docker-Compose
* Sample Repositories for WA

### 2. Related work:
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
