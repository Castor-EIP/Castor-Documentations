---
title:          Beta Test Plan Castor
subtitle:       Castor Application - Desktop Application for video recording/streaming
author:         Castor Application - Castor Team
module:         G-EIP-700
version:        1.3
---

# Beta Test Plan – Castor

## 1. User Roles

| Role         | Description                                            |
| ------------ | ------------------------------------------------------ |
| Regular User | Can create scenes, stream, record, and manage sources  |
| Pro User     | Regular User Access + AI tools access in multicam mode |

---

## 2. Core Functionalities in Scope

| **Feature ID** | **User Role** | Feature Name                  | Description                                                          | Priority | Notes                                    |
| -------------- | ------------- | ----------------------------- | -------------------------------------------------------------------- | -------- | ---------------------------------------- |
| F1             | Everyone      | Streaming                     | Stream a scene to an RTMP endpoint                                   | High     | Manual RTMP or platform-managed stream   |
| F2             | Everyone      | Recording                     | Record a single scene as MP4 format                                  | High     | File integrity and correctness validated |
| F3             | Everyone      | Scenes Management             | Create and manage multiple scenes with different sources             | Medium   | Functional rendering only                |
| F4             | Everyone      | Scene Switching               | Switch scenes during streaming or recording                          | Medium   | No interruption allowed                  |
| F5             | Everyone      | Multicam                      | Switch between multiple physical camera inputs dynamically           | Medium   | Manual switching only                    |
| F6             | Everyone      | Streaming Platform Management | Authenticate and control streaming platforms from Castor             | Low      | OAuth or RTMP key supported              |
| F7             | Pro User      | AI Agent Mode                 | Allow Ai to access and advice the user about cam switch              | High     | F4 completion is needed to run this task |
| F8             | Pro User      | AI Auto Mode                  | Allow Ai to access and control the stream/record cameras             | High     | F4 completion is needed to run this task |
| F9             | Everyone      | Create Account                | Register informations and preferences of a user into Castor DataBase | Medium   | Via the website or the application       |
| F10            | Everyone      | Connect                       | Connect the account to Castor Application                            | Medium   | Tested on application side               |

---


## 3. Beta Test Scenarios

### Scenario 1: Streaming

- **Roles:** Regular User, Pro User  
- **Objective:** Verify that a scene can be streamed successfully via RTMP.
- **Preconditions:** A valid RTMP URL and stream key (manual or platform-provided).

- **Test Steps:**
	1. Open the Scene window.
	2. Create a scene with at least one video source.
	3. Navigate to the Studio window.
	4. Click on "Start Streaming" button.
	5. Select the scene to stream.
	6. Choose the streaming platform or manual RTMP.
	7. Click on "Start" button.

- **Expected Result:** The selected scene is live on the target platform or RTMP endpoint without errors.

---

### Scenario 2: Recording

- **Roles:** Regular User, Pro User  
- **Objective:** Verify that a scene can be recorded correctly in MP4 format.
- **Preconditions:** None.

- **Test Steps:**
	1. Open the Scene window.
	2. Create a scene with at least one video and one audio source.
	3. Navigate to the Studio window.
	4. Click on "Start Recording" button.
	5. Select the scene to record.
	6. Select MP4 as the output format.
	7. Click on "Start" button.
	8. Click on "Stop" button recording after a short duration.

- **Expected Result:**
	- An MP4 file is created.
	- The file is readable.
	- Video playback is correct (no visual corruption).
	- Audio playback is present and synchronized.

---

### Scenario 3: Scenes Creation and Rendering

- **Roles:** Regular User, Pro User 
- **Objective:** Verify that scenes can be created and rendered correctly.
- **Preconditions:** None.

- **Test Steps:**
	1. Create a scene with one video source and one audio source.
	2. Create a second scene with two video source and one audio source.
	3. Create a third scene with one video source and two audio sources.

- **Expected Result:**
	- All scenes are created successfully.
	- Each scene renders correctly when selected.
	- No validation of audio mixing or visual composition logic is required.

---

### Scenario 4: Scene Switching During Stream or Recording

- **Roles:** Regular User, Pro User  
- **Objective:** Verify that scene switching works without interruption.
- **Preconditions:** Scenario 3 completed.

- **Test Steps:**
	1. Start a stream or recording.
	2. From the Studio window, select another scene.

- **Expected Result:**
	- The active scene changes immediately.
	- No stream or recording interruption occurs.

---

### Scenario 5: Multicam

- **Roles:** Regular User, Pro User
- **Objective:** Verify dynamic switching between camera inputs.
- **Preconditions:** A scene configured with multiple camera sources.

- **Test Steps:**
	1. Start a stream or recording.
	2. Open the Multicam window.
	3. Select a different camera.

- **Expected Result:**
	- The active camera changes instantly.
	- No interruption or stream/record failure occurs.

---

### Scenario 6: Streaming Platform Management

- **Roles:** Regular User, Pro User  
- **Objective:** Verify platform authentication and stream control from Castor.
- **Preconditions:** F10

- **Test Steps:**
	1. Open the Settings window.
	2. Access platform account management.
	3. Authenticate using OAuth **or** configure a manual RTMP key.
	4. Return to the Studio window.
	5. Start a stream.
	6. Stop the stream from Castor.

- **Expected Result:**
	- Platform account is connected successfully (if OAuth).
	- Stream can be started and stopped without visiting the platform website.

### Scenario 7: AI Agent Mode

- **Roles:** Pro User  
- **Objective:** Use provided AI to advice camera switch.
- **Preconditions:** F4 completion

- **Test Steps:**
	1. Setup your scenes
	2. Select the Agent Mode of the AI
	3. Select the adapted AI
	4. Start Live/Record

- **Expected Result:**
	- Overlay around adviced cameras for a switch.

### Scenario 8: AI Auto Mode

- **Roles:** Pro User  
- **Objective:** Use provided AI to control a stream by its own.
- **Preconditions:** F4 completion

- **Test Steps:**
	1. Setup your scenes
	2. Select the Auto Mode of the AI
	3. Select the adapted AI
	4. Start Live/Record


- **Expected Result:**
	- Camera switch using Castor AI during record an stream.

### Scenario 9: Create Account

- **Roles:** Everyone
- **Objective:** Register a Castor Account
- **Preconditions:** None.

- **Test Steps:**
	1. Go to the official website (url not defined yet)
	2. Click the "Create Account" Button
	3. Fill the asked informations in the corresponding labels.
	4. Click the "Register" Button


- **Expected Result:**
	- A new account as been created with user's connection informations.
### Scenario 10: Create Account

- **Roles:** Everyone
- **Objective:** Register a Castor Account
- **Preconditions:** F9

- **Test Steps:**
	1. On the app, click the account button
	2. Click the "Connect" Button
	3. Fill the asked informations in the corresponding labels.
	4. Click the "Connect" Button


- **Expected Result:**
	- The user might be registered on the app
	- The user can now exec F6

---

## 4. Success Criteria

The success of the beta version is evaluated through **measurable functional outcomes** based on the execution of the defined test scenarios. Each feature is validated using concrete indicators collected during beta testing.

| **Feature ID** | **Key success criteria**                                                                                   | **Indicator / Metric**                                                                                                                       | **Result**      |
| -------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | --------------- |
| F1             | A user can successfully start and maintain an RTMP stream without application errors                       | 10 streaming attempts, stream successfully started and maintained in at least 8 cases **-(Possibilité de rajouter un indicateur de temps)-** | To be evaluated |
| F2             | A user can record a scene and obtain a valid MP4 file                                                      | 10 recordings performed, 10 MP4 files created and readable with correct audio/video                                                          | To be evaluated |
| F3             | Scenes created by the user render correctly when selected                                                  | 15 scene selections, 0 rendering failure                                                                                                     | To be evaluated |
| F4             | Switching scenes during streaming or recording does not interrupt the process                              | 10 scene switches during active stream/recording, 0 interruptions                                                                            | To be evaluated |
| F5             | Switching between physical camera inputs updates the active video source correctly                         | 10 multicam switches, correct camera displayed each time                                                                                     | To be evaluated |
| F6             | A user can authenticate (OAuth or RTMP key) and fully control a stream from Castor                         | 5 platform connections tested, start/stop stream successful in all cases                                                                     | To be evaluated |
| F7             | A user determine if the amount of proposed camera switch and their consistency is relevant of an action    | 60% of adviced camera switch approved by the user (by switching to the proposed camera)                                                      | To be evaluated |
| F8             | A user determine if the amount of automatised camera switch and their consistency is relevant of an action | 50% of average notation on a feedback pop up after a stream                                                                                  | To be evaluated |
| F9             | A user can create his account easily on the dedicated website                                              | 90% of successful creation on the website                                                                                                    | To be evaluated |
| F10            | A user can connect his account easily on the app                                                           | 90% of successful connection on the app in order to realyse F6                                                                               | To be evaluated |

---

## 5. Known Issues and Limitations

| Issue              | Description                                      | Impact              | Planned Fix |
| ------------------ | ------------------------------------------------ | ------------------- | ----------- |
| AI Limitations     | AI tools limited to specific content types       | Feature unavailable | Yes         |
| Source Limitations | Performance depends on hardware and source count | Quality / framerate | Yes         |

---

## 6. Conclusion

This beta test plan focuses on validating the core functionality of the Castor application in realistic streaming and recording conditions. The collected feedback and metrics will allow the team to identify critical issues, validate feature readiness, and prepare the foundation for the final product release.

