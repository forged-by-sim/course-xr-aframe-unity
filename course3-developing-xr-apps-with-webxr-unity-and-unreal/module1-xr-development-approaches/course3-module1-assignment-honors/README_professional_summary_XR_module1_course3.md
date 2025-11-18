Rhomaleosaurus 3D Viewer – A-Frame WebXR Scene

Course 3 – Module 1 | XR Development | A-Frame | WebXR

This scene served as the launchpad for a broader WebXR pipeline. The project began as a simple goal—load and display a 3D model in a browser-based A-Frame scene—but quickly evolved into a multi-layered debugging and learning experience involving GLB integrity, CORS restrictions, model topology, coordinate issues, and animation playback challenges.

The final result was a fully interactive, animated 3D viewer featuring a marine reptile, complete with proper placement, camera controls, and smooth movement—all running in-browser using A-Frame and animation-mixer.

Project Objective

Build a lightweight, embeddable WebXR scene using A-Frame that:

Loads a 3D Rhomaleosaurus model via gltf-model

Plays an idle swim animation

Uses orbit controls for rotation

Prepares groundwork for later VR and AR extensions

Scene Architecture

The base A-Frame scene included:

A ground plane

A red cube for visibility reference

Lights (ambient and point)

A camera with orbit controls

A GLB model entity positioned into view

This provided a functional layout for debugging geometry, positioning, and camera motion.

Technical Challenges & Debugging Highlights

1. Model Not Appearing at All
The Rhomaleosaurus GLB file would not show up in the scene despite correct pathing. The inspector confirmed the entity existed but without visible geometry.

Attempts made:

Switching between .gltf and .glb

Adjusting scale, position, and rotation

Testing visibility toggles

Inspecting the A-Frame scene tree

The culprit was a silent CORS restriction.

2. CORS Blocking GLB Loading
The browser console showed a familiar error:
“Access to fetch at file:///… has been blocked by CORS policy.”

This clarified that local model loading doesn’t work via file://. A web server was needed.

Fix:
Started a local Python server with python -m http.server, then accessed the scene via http://localhost:8000, which successfully loaded the model.

3. Model Appearing as a Speck
Once CORS was fixed, the model appeared—but only as a floating dot or ghost shape. This was caused by:

A massive bounding box

Microscopic scale

Incorrect pivot origin

Model spawning behind the camera

Solution:
Manually adjusted A-Frame entity properties to:

position="0 2 -0.1"

rotation="0 180 0"

scale="0.5 0.5 0.5"

This centered the creature in front of the camera at eye level.

4. Flat Fossil Model Issue
The original Rhomaleosaurus was a 3D scan of a flat fossil slab. It lacked depth and was unusable for VR/AR placement or animation.

Lighting didn’t reveal details. Rotation revealed a paper-thin structure.

This model was abandoned.

5. Switched to Pistosaur_Animated.glb
A better model was sourced—fully 3D, smooth topology, and included built-in swim animation. To maintain naming consistency, only the entity ID was changed to “rhomaleosaurus.” The file itself remained unchanged.

6. Animation Didn’t Auto-Play
After replacing the model, it appeared fully but was frozen.

Fix:
A-Frame requires the animation-mixer component to activate embedded GLTF animations. Once added, the model swam in place as expected.

7. Orbit Controls Broken at First
Camera orbiting failed due to missing scripts and incorrect rigging.

Fix:

Imported aframe-extras.js

Nested the camera correctly

Set target to the correct entity ID

This enabled user rotation around the model.

Final Scene Setup

A pistosaur model rigged to swim smoothly

Correct position, rotation, and scale

Embedded animation running automatically

Orbit camera working via mouse input

Local server hosting via Python

Structured and minimal HTML file organization

Lessons Learned

CORS is an unavoidable reality in WebXR — always use a local or hosted server

Flat 3D scans do not always translate to usable 3D assets

The A-Frame Inspector is invaluable for real-time debugging

Model placement depends on invisible origin and bounding box awareness

Not all animations auto-play — animation-mixer is essential

Orbit controls require clean rig setup and extra libraries

Always isolate problems in a simplified test scene before scaling up

Professional Outcome

This scene marked the transition from asset loading to interactive prototyping. It laid the groundwork for future VR and AR modules by teaching the fundamentals of model structure, A-Frame architecture, and the invisible rules of WebXR behavior.

Every challenge solved here became a stepping stone for more complex builds—turning a simple viewer into a professional-grade XR learning milestone.