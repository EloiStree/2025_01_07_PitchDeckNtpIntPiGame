Important Check:
- Does the game works offline
  - () Does the game work as 2D test zone ? 
  - Quest are connected to the wifi
  - PC/Phone of Monitor is connected to Wifi
  - Is NTP Sync (Outter Wild planets)
  - Is message monitor send are received
  - Is killing the bugs are sync ?
  - Is Enter the code is sync ?
  - Is all bugs killed are sync ?
  - Is all missions complete are sync ?
    - Do we compute the missions part on any player or just the monitor
      - If only the monitor, it means that game must have monitor to end  
  - () Calibration
    - Is game loadable with 1x2 meter ?
    - Is game loadable with 1x3 meter ? 
    - Is game loadable with 1x5 meter ?
    - Is game loadable with real life triangle ?
    - Is game movable/adjustable by "hand" ?
      - () Is game reloadable from previous Guardians ?
    - Game is recalibrated when ...
      - Player quit and come back in game ?
      - Player press accidently the relocation buttons ?
      - Game crash and player comeback in it ?
      - Game crash is reloaded with a new (previous) guardian ?
  - ADB;
    - Does connect the Android devices to the PI,or mini PC, turn it to a wifi adb server ?
    - Does going in the application that  are ban redirect player in the game ?
    - Does ADB take random screenshot of the game to give context to monitor ? 

Basic
- is pi configure ?
- is pi connectable by pi connect ?
- is pi has public ssh ?

Install on pi
- Is NTP insall on pi?
- is trusted websocket install on pi?
- is flask install on pi?
  - at least 8080 /hostname ?
- are port 22 123 80 8080 4615 4625  open ?

Unity 3D
- Add those important package
  - https://github.com/EloiStree/OpenUPM_DeveloperNote.git
  - https://github.com/EloiStree/OpenUPM_TickCollection.git
  - https://github.com/EloiStree/2025_04_02_FacadePrimitiveValueRelay.git
  
Int Lobby: 
- Copy packages of https://github.com/EloiStree/2025_03_11_NtpWsClientIntegerLobbySetup
  - Project Monitor
  - Project XR
- Minimal:
  - Add Trusted Websocket Client PI for PI
    -  https://github.com/EloiStree/2025_03_11_NtpWsClientIntegerLobbySetup
  - Add Static Int Lobby Bridge with Broadcaster
    - https://github.com/EloiStree/2025_03_18_IntLobbySampleSpaceship.git 
- Demo 
  - Add SpaceShip Sample
    - Game Lobby Prefab for XR
    - Monitor Lobby Prefab for the Phone


- I need to know when a blob die or spawn
- I need to know (if not my code ) what is the pourcent state of game
- I need to know when the code is enter
- We need to know how to relaod the scene (reset or scenemanager ?) 
  

Game to Facade GF
Facade to Game FG
- Check List to link
- How do we
  - Link the monster death and spawn
- Where do we put the host code ?
  - Libutir  
  - GF:  List of Monster as gameobject ot enable disable
    - Or: Code that notify that Monster is death and spawn
  - GFG: Game Time ?
  - GF: Enter Password
 
Relocation using three points in space:
- Add Tag Triangle
  - Add Triangle 1x5
  - Add Triangle 1x3
  - Add Triangle Three Window to door
- Add Cursor ThreePoints
  - Add calibration point
- Add Facade with what gameobject level need to me moved
  
Relocation Memory using Guardian Triangle ID
- Add Transform3 to represent the guardian
- Add custom code to generate triangle when guaridan is loaded
- Add code to move the room (in addition to the movable three point space
  - Xbox controller https://github.com/EloiStree/2025_04_09_XboxKeyboardCalibration 
  - Press all buttons to move scene technique (Look for old code)
- When Move trigger code to save relocation
- Add button to force "Find and reload"


---------

R&D: 
- Use image in the Van to reset code ?
- Use Depth API to generate a runtime guardian ?


------------

============

What I had in mind
- A game is launch every 5 minutes
- Player wait in lobby for next game
- The same game happen to everyone
- The goal is to understand what happened
- Mini game are playble offline

Technicality added 
- some interaciton are possible with IID
  - One is death game is lost 
- Asked: game can be relaunch ( offseted)

_____________

Note of future project: 
- Make a websocket server on the pi that allows to share screenshot of current camera feed for monitoring
=

