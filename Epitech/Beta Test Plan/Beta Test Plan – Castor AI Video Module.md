---
title:          Beta Test Plan
subtitle:       Castor AI – Video Analysis Module
author:         Castor AI - Castor Team
module:         G-EIP-700
version:        1.1
---

## **1. Project context**

---

## **2. User Roles**

The following roles will be involved in beta testing.

| **Role Name** | **Description** |
|--------------|----------------|
| Administrator | Manages system initialization, video sources, and AI configuration |
| AI Operator | Launches video analysis and monitors AI execution |
| Developer | Observes system behavior, logs, and technical stability |

---

## **3. Feature table**

All of the listed features will be demonstrated during the beta presentation.

| **Feature ID** | **User role** | **Feature name** | **Short description** |
|--------------|---------------|------------------|-----------------------|
| F1 | Administrator | AI system initialization | Initialize the AI core and video analysis modules |
| F2 | Administrator | Video source selection | Select a video source (file or live camera) |
| F3 | AI Operator | Pre-recorded video loading | Load a pre-recorded foot video |
| F4 | AI Operator | Live camera connection | Connect a camera as a live video input |
| F5 | AI Operator | Video stream processing | Process video frames through the AI pipeline |
| F6 | AI Operator | Real-time analysis | Perform AI analysis during video playback or live stream |
| F7 | AI Operator | Result generation | Generate structured analysis results from the video |
| F8 | Developer | Error handling | Handle invalid video sources or connection issues |
| F9 | Developer | Performance monitoring | Monitor processing latency and stability |
| F10 | Developer | Live demonstration | Execute a full live demo without blocking failure |

---

## **4. Success criteria**

| **Feature ID** | **Key success criteria** | **Indicator/metric** | **Result** |
|--------------|--------------------------|----------------------|------------|
| F1 | AI initializes without errors | 10 launches, 0 initialization failure |  |
| F2 | Video source can be selected | 5 selections, all successful |  |
| F3 | Pre-recorded video loads correctly | 5 videos tested, 0 loading error |  |
| F4 | Live camera connects correctly | 3 connections, 0 crash | |
| F5 | Video frames are processed continuously | No frame drop > 5% | |
| F6 | AI analysis runs during playback | Analysis active on 100% of video duration | |
| F7 | Results are generated and usable | Outputs follow defined structure | |
| F8 | Errors are handled gracefully | Clear error messages in all failure cases | |
| F9 | Processing latency remains acceptable | Average latency < 200 ms per frame |  |
| F10 | Live demo completes successfully | No blocking issue during presentation | |

