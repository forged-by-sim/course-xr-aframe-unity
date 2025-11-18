🦖 Rhomaleosaurus WebXR & WebAR Experience
XR Course 3 – Honors Project (A-Frame + Blender + MyWebAR)

This project showcases a complete XR pipeline built around a scientifically inspired Rhomaleosaurus model. The experience spans two platforms:

A-Frame WebXR viewer (VR-style 3D exploration)

Marker-less WebAR experience (place the animated creature into real space)

The final AR scene works directly through a mobile browser, requires no app download, and demonstrates an accessible, lightweight approach to XR deployment.

🌊 Project Overview

The goal of this project was to create an interactive prehistoric sea-reptile experience that could exist both in a virtual museum-style viewer and in real-world AR. Users can rotate around the model in WebXR and physically walk around it in WebAR, observing an animated Rhomaleosaurus swimming in place.

This project evolved through multiple platforms—Blender, Unity, A-Frame, and MyWebAR—culminating in a cross-device XR experience that preserves animation, presence, and accessibility.

🛠 Tools & Technologies

Blender
Rigging the Rhomaleosaurus, creating a bone hierarchy, and exporting animation via GLTF/GLB.

A-Frame (WebXR)
Building a VR-style orbit viewer with animation-mixer, custom lighting, and scene controls.

Python Local Server
Testing early WebXR AR capabilities over LAN.

Unity (Attempted)
Explored for AR Foundation/WebXR builds; ultimately pivoted due to mobile animation issues.

MyWebAR
Final hosting solution for fully animated, marker-less WebAR on both iOS and Android.

🧩 Development Journey
Stage 1 — Rigging & Preparing the Model

The project began in Blender, where the Rhomaleosaurus was manually rigged. Bones were assigned to all major body parts, especially the flippers, to create a smooth swimming cycle. The final animation was exported as a .glb with WebXR compatibility in mind.

Earlier Unity exports revealed animation inconsistencies, which prompted the shift toward browser-based XR.

Stage 2 — A-Frame WebXR Viewer (VR-Style 3D Model)

A full WebXR viewer was developed using A-Frame’s <a-gltf-model> and animation-mixer.
This version allowed users to:

Orbit around the creature

View looping animation

Experience a clean museum-style environment

Access the scene on desktop or mobile

This viewer served as the foundation of the project and was later recorded for submission and portfolio use.

Stage 3 — Exploring Marker-less AR in A-Frame

Marker-less AR was attempted using WebXR’s hit-test feature.
Testing revealed platform limitations:

iOS Safari required .usdz files (not supported by A-Frame without additional pipelines)

Android Chrome partially worked but lacked stable anchoring

Local testing via Python server suffered firewall restrictions and connection issues

While these experiments didn’t produce a stable AR scene, they informed the next pivot and helped clarify WebXR’s practical limits across devices.

Stage 4 — Final AR Deployment with MyWebAR

The final, working AR scene was created using MyWebAR, a browser-based platform supporting animated GLB models and marker-less placement.

Features of the final AR build:

Fully preserved swimming animation

No markers required

Direct mobile link access

QR code support

Works on both iOS and Android

Screenshots and screen recordings captured from iPhone

The final AR experience successfully recreates the illusion of the Rhomaleosaurus floating in real space.

🎬 Recorded Media

Two polished videos document the experience:

Rhomaleosaurus Viewer – A-Frame WebXR

AR Scene – Rhomaleosaurus Swims (MyWebAR)

Additional screenshots include the QR code, model placement, lighting variations, and museum-style VR viewer.

(You can embed your videos and images here once they’re uploaded to GitHub.)

✏️ Key Interactions

The core interaction in this project is spatial exploration, not touch-based UI.
Users engage with the creature by:

Physically walking around it

Viewing the animation from different angles

Observing scale within real-world context

Exploring motion and silhouette naturally

In the WebXR viewer, users orbit the model much like a 3D museum exhibit.

🧠 Reflection

This project represents a full XR toolchain journey—from Blender rigging to Unity testing, A-Frame building, and WebAR deployment. Several major insights emerged:

XR development often requires pivoting between toolchains

WebAR is highly sensitive to platform differences

Mobile AR must account for device, browser, and network constraints

Browser-based XR can be powerful, lightweight, and widely accessible

The simplest tool is sometimes the best tool for the job

The most rewarding moment was seeing the animated Rhomaleosaurus swimming in my own space with nothing but a browser. It demonstrated how immersive XR can become through minimal interaction and strong environmental grounding.

🚧 Troubleshooting Notes (Summary)

A complete breakdown of failed approaches is documented in the troubleshooting file.
Key lessons include:

Unity animations did not reliably transfer to mobile AR builds

A-Frame WebXR AR has limited iOS support without .usdz conversion

Local LAN hosting for AR testing is prone to firewall and network obstacles

WebAR requires thoughtful model compression and cross-device testing

These challenges guided the final pivot to MyWebAR for stability and cross-platform compatibility.

(Full detailed troubleshooting is preserved in your AR scene_Troubleshooting 5_AFrame.txt.)

📁 Repository Structure

This folder contains:

A-Frame WebXR viewer files

AR media recordings

Blender rigged model exports

Assignment breakdowns

Troubleshooting documents

Final AR assets (GLB, QR codes, screenshots)

Submission-ready summaries

Each file is preserved so developers and instructors can understand the process from start to finish.

💡 Future Improvements

Adding tap-based interactions in AR (rotation, facts panel toggles)

Exploring USDZ export pipelines for native iOS AR support

Compressing GLB for faster WebAR load times

Adding spatial audio or educational narration

Deploying both experiences on a dedicated project webpage

🙌 Acknowledgements

This project was created as part of Extended Reality for Everybody – Course 3.
The workflow represents a blend of experimentation, troubleshooting, and cross-platform XR development.