Summary of Key Interactions & Reflection
Key Interactions

This AR scene builds on the earlier VR viewer by allowing the Rhomaleosaurus model to be placed and animated in real-world space using marker-less WebAR. The key interaction is the user’s ability to physically move around the model with their smartphone or tablet, observing the prehistoric sea reptile as it swims in place, creating the illusion of it floating in their environment.

Rather than rely on touch gestures or on-screen UI, the implicit interaction is spatial: users explore the model by walking around it. This supports experiential learning, especially relevant for educational or museum-style settings.

While this version does not include object manipulation (e.g., tap to rotate), it does include looped animation, giving the illusion of life. Marker-less AR was chosen for its accessibility, and users can activate the experience using a direct link or QR code without needing a printed marker or dedicated app.

Reflection

The development process began in Unity, but I encountered significant challenges with maintaining animation playback in mobile AR, particularly in hosted scenes. After multiple troubleshooting rounds (including exporting from Blender, converting to FBX/GLB, and re-rigging), I pivoted to a more Web-friendly format using A-Frame and ultimately hosted the final AR scene using MyWebAR.

The hardest part was navigating technical inconsistencies across platforms. For example, WebXR AR worked well on Android Chrome but was unsupported in iOS Safari unless converted to USDZ. Additionally, hosting local WebXR servers on a Surface Pro with firewall issues created several delays.

The easiest and most rewarding part was seeing the rigged Dino swimming in my own space, using nothing but a browser. It was a powerful moment of realizing that XR can be both lightweight and immersive, and that sometimes pivoting tools is part of the real development process.

Questions for Peers

Have any of you successfully deployed a marker-less A-Frame AR scene that supports object interaction or UI toggles? If so, what libraries or toolkits did you use?

What strategies or tools have worked best for compressing GLB models for smooth WebAR playback?

If I wanted to evolve this project into an interactive educational AR installation, what input methods (gaze, tap, menu) would you recommend?







![Assignment 3](QR code_AR experience is live.png)

![Assignment 3](AR Scene_Dino_Rhomaleosaurus.mp4)

![Assignment 3](AR Scene_Rhomaleosaurus_Swims.mp4)

![Assignment 3](Rhomaleosaurus_left.png) 

![Assignment 3](VR Scene_Rhomaleosaurus_Viewer_A-Frame.mp4)

![Assignment 3](VR Scene_Triceratops Model Viewer_A-Frame.mp4)




