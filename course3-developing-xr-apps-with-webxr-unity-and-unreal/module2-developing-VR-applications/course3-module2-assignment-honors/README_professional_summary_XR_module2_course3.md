🥽 Rhomaleosaurus VR Scene (Unity + Blender Pipeline)
XR Course 3 – Module 2 Honors Project: Rigged Model Viewer for VR

This project documents the full workflow of preparing, importing, and deploying a rigged Rhomaleosaurus model from Blender into Unity for a VR scene — and eventually, an AR scene using Unity’s AR Foundation. It includes breakdowns of file preparation, prefab variant creation, import failures, and critical troubleshooting insights that helped stabilize the pipeline.

🧠 Project Goal

The goal was to build an immersive VR experience using Unity that presents a rigged, lifelike Rhomaleosaurus. The scene simulates the sensation of observing a prehistoric creature glide through an underwater world — with accurate camera placement, prefab management, and an expandable structure for AR.

This project lays the foundation for a cross-platform deployment pipeline:
Blender → Unity (VR) → Unity (AR).

🛠 Toolchain Overview

Blender — Rigging, weight painting, animation preparation

Unity 6.2 — Scene setup, prefab creation, camera/framing

GLB Viewer (reference) — Cross-checking textures and rig animation

FBX (.fbx) — Export format for Unity

Prefabs + Prefab Variants — Clean hierarchy management

🧩 Development Breakdown
Step 1 — Rig Prep in Blender

Rigged mesh using Armature system

Shift-selected mesh + bones

Applied all transforms (Ctrl + A)

Configured proper FBX export settings (Y-up, -Z forward, Apply Unit/Modifiers)

Final export:
Rhomaleo_Weighted_UNITY_FINAL_FIXED.fbx

Step 2 — Import into Unity & Create Prefab

Imported .fbx into Unity > Assets > Models_RHOMA > Rigged

Verified import settings:

Scale: 1.00

Convert Units: On

Preserve Hierarchy: On

Generate Colliders: Off

Created a Prefab Variant for editing without breaking the original import

Step 3 — Prefab Scene Placement

Initial attempts to drag the prefab into the scene failed.

💡 Solution:
Used "Replace With Prefab" from an empty GameObject — this successfully instantiated the model.

Step 4 — Positioning & Visibility

Prefab placed at (0, 0, 0) seemed invisible.
Turns out it was out of camera view — re-centering the scene camera made it visible again.

Lesson:
“Disappearing” prefabs might just be off-screen or under terrain.

Step 5 — Cross-Referencing GLB

Opened rhomaleosaurus_high.glb in a viewer to compare:

Texture smoothness

Rig alignment

Material rendering

This guided the Unity scene framing and lighting decisions.

Step 6 — Preparing for Animation

While Blender’s FBX export included animation strips, Unity requires:

Animator Controller

Timeline configuration or

Manual animation clip setup in the Rig tab

This was deferred to the AR scene phase.

🧯 Troubleshooting Highlights

This project included multiple rigging, import, and prefab errors, including:

Stylus input failures in Blender (couldn’t extrude bones)

FBX files importing into Unity with missing mesh or bone-only spaghetti

Viewer preview mismatch (accidental bee model from Windows cache 🐝)

Unity refusing to drag working prefabs into the scene

Static FBX versions that only included Armature (mesh deselected during export)

✅ All were overcome by:

Applying consistent export settings

Selecting both mesh + armature

Using prefab replacement methods

Avoiding 3D viewer assumptions (always test in Unity directly)

Each challenge deepened practical understanding of Unity’s import quirks, Blender’s FBX options, and how to prep animation-ready prefabs for XR.

🎮 Final VR Scene Outcome

By the end of the module, the project included:

A rigged dinosaur prefab positioned and scaled accurately

A VR-ready Unity scene with camera and lighting

Clean hierarchy via prefab variant

A reusable model for upcoming AR deployment (Course 3, Module 3)

💡 Lessons Learned

Unity’s prefab system is powerful — but fragile when hierarchy breaks

Blender’s export needs tight control (transforms, bone axis, unit scale)

Prefab visibility issues are usually scene framing problems

3D viewers lie — test everything in-engine

Stylus/touchscreen setups may not work well with Blender rigging tools

Export checklists save hours on Unity re-imports

🧭 Next Steps

Build AR scene using Unity’s AR Foundation

Add animation playback (swim cycle) in Unity Timeline or Animator

Add touch interactions (e.g., tap to place, rotate)

Explore integrating Unity Recorder or ARKit for screen capture

Host a comparison between A-Frame and Unity outcomes (browser vs engine)

📂 What’s Inside This Folder

VR scene_Unity_AssignmentBreakdown4.txt → Full prefab integration notes

VR scene_Troubleshooting 4_Unity.txt → Detailed rigging + Unity import issues

.fbx files → Final rigged export

.glb file → Visual reference

Prefabs/ → Instantiable variants for Unity scene
