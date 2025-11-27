# 🧊 Technical Specification
**Project:** *"Northbound"*
**Genre:** survival horror with psychological thriller elements
**Platforms:** iOS / Android / PC
**Developer:** game development team
**Client:** educational project

-----
## 1\. Introduction
The *"Northbound"* project is an atmospheric **horror** game set in the eternal cold and solitude of the Arctic.
The player finds themselves at an abandoned polar station where something inexplicable is happening. To survive and uncover the mystery of the expedition's disappearance, one must explore locations, collect clues, and use the device's camera to capture "anomalies," as well as geolocation to activate certain events depending on the player's location.

The main idea of the project is to **create an effect of complete immersion**, where the player's reality gradually blends with the game through camera and GPS technologies.

-----
## 2\. Goals and Objectives
### Goals:
- Develop an interactive horror game with a unique Northern atmosphere.
- Implement the use of camera and geolocation to enhance immersion.
- Create a story based on psychological tension and loneliness.
### Objectives:
1. Develop a game prototype with one main location — a polar station.
1. Implement a mechanic for photographing clues through the device's camera.
1. Add geolocation events (for example, activation of audio hints when moving).
1. Create an inventory system and clue journal.
1. Develop visual and sound design that enhances the atmosphere of fear and cold.
-----
## 3\. Functional Requirements
### Main functions:
- **Character movement** through location (3D/first-person).
- **Use of device camera:**
  - photographing clues;
  - displaying «hidden» world elements through viewfinder;
  - saving snapshots to journal.
- **Geolocation:**
  - events activated at specific real coordinates of the player (optional);
  - atmosphere changes (for example, different weather effects depending on region).
- **Inventory:** storage of clues, batteries, first-aid kits.
- **Journal:** notes, photographs, remarks.
- **Status system:** level of warmth, fatigue, mental state.
- **Story scenes and dialogues:** activation upon meeting conditions.
-----
## 4\. Interface Requirements
### Main screens:
- **Main menu:**
  - New game / Continue / Settings / Exit
- **Game HUD:**
  - temperature, stamina, flashlight battery indicators;
  - camera open button;
  - mini-map or compass.
- **Camera interface:**
  - central crosshair;
  - Take photo» button;
  - AR filter activation button;
  - view of taken snapshots.
- **Journal:**
  - tabs: "Notes", "Photos", "Clues";
  - ability to link found elements.
### Visual style:
- Cold color palette: white, blue, gray, muted tones.
- Minimalist interface without unnecessary elements.
- Camera effects: noise, distortions, grain.
-----
## 5\. Non-functional Requirements
- **Performance:** stable operation at 30+ FPS on mid-range devices.
- **Security:** use of camera and geolocation only with user permission.
- **Privacy:** geodata and photos are not transmitted to server without explicit consent.
- **Compatibility:** ARCore (Android) and ARKit (iOS) support.
- **Stability:** the game must work correctly without internet access (offline mode).
- **Scalability:** ability to add new locations and scenarios.
-----
## 6\. Integrations and Environment
- **Game engine:** Unity 3D (preferred) / Unreal Engine 5.
- **Libraries and SDK:**
  - ARCore / ARKit for camera and augmented reality functionality;
  - GPS API for coordinate determination;
  - Firebase for analytics and progress storage (optional).
- **System requirements:**
  - Android 8.0+ / iOS 13+;
  - minimum 3 GB RAM;
  - 8 MP camera and higher.
-----
## 7\. Limitations and Assumptions
- User may deny access to camera and geolocation — the game must remain playable.
- Images taken through the camera are stored locally only.
- AR usage is not possible on all devices — a non-AR mode is required.
- Events dependent on geolocation should not require constant GPS monitoring (battery saving).
- The game does not contain realistic scenes of violence, blood or shock content (age rating 16+).
-----
## 8\. Acceptance Criteria

|No|Criterion|Description|
| :-: | :-: | :-: |
|1|Gameplay|Player can complete the story from beginning to end without errors or freezes.|
|2|Camera|Photo capture works, images are saved to the diary, AR mode functions on supported devices.|
|3|Geolocation|Events are correctly activated when the player moves.|
|4|Interface|All elements are readable, do not obstruct the view, work correctly on different screens.|
|5|Optimization|FPS not lower than 30 on mid-range devices.|
|6|Security|Permission requests for camera and geolocation are displayed before use begins.|
|7|Atmosphere|Alignment of visual and audio style with horror and Arctic themes.|

-----
## 9\. Appendices
### 9\.1 Location Concept Art
- Abandoned polar station
- Ice caves
- Northern lights
### 9\.2 Mission Scenario Example
**Mission:** "Station Echo"

- The player finds a destroyed antenna block.
- Need to photograph a symbol on the wall through the camera.
- After the photo, an audio signal activates — a whisper indicating the path to the next point.
- If geolocation is active and the player is in a zone with latitude > 60°, a "blizzard effect" is activated.
### 9\.3 List of Development Tools
- Unity 3D
- Blender (3D models)
- Adobe Photoshop / Illustrator (textures, interface)
- Audacity / FMOD (sound design)
