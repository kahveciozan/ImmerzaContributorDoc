# Contributor Documentation IMMERZA VR
This document is prepared as a roadmap for designers and developers who want to contribute to the IMMERZA VR application

Meditation App for Oculus Quest 2 
![Error](https://github.com/kahveciozan/LaylaVR/blob/public/Assets/Sprites/LaylaLogo.png)
## What is IMMERZA
Layla is a meditation application that aims to be published first on Applab(Sideqestvr.com) and then on Oculus Official Store.Target devices are Oculus Quest and Quest2. Currently, we have decided to consist of 3 main categories. Focus, Calm and Excitement. You can specify ideas for new category ideas. Each part should consist of 2 or 3 different parts(With different environments).

## Guidelines for Creating Content IMMERZA. Be a contibutor.
[Click here to become a contributor](https://forms.gle/XvepfJQD45Uu37mT7) <br/>
Layla were created using the Unity3D Game Engine

### How To Create a New Scene and Environment
1. Create and develop your scene in your own project. (Use Unity Version 2021.3.11.X) 
2. Decide in which category you want to create a scene. Then create one new scene.
3. Delete Maincamera.
4. Add  `OvrCameraRig.prefab` to Hierarchy. This prefab includes Darker Effect, some particle effects(virtual breahing etc.) UI(loading screen, mood tracker, rating panel and finish panel).
5. Desing your original scene.
6. You can add our ready-mate exercises to your own scene. [Prefabs](https://www.exampleprefab.com)
7. Add Addressables library(Addressable Version 1.19.11.) to your unity project. This is very important. Otherwise there may be problems loading the scenes.
8. Build the scene with Addressable Default Build.
9. Addressables will give 4 files (two .bundle, one json and hash file)
10. Upload these 4 files to the website respectively.
11. Add title and description.
12. Finally click the save button.
13. You can update the scene whenever you want.
14. 
### Development Tools and SDKs
[Unity3D Game Engine](https://unity.com/) <br/>
[Oculus Integration SDK](https://assetstore.unity.com/packages/tools/integration/oculus-integration-82022) <br/>
[Adressable Version 1.19.11.] <br/>
[DOTween(HOTween v2)](https://assetstore.unity.com/packages/tools/visual-scripting/dotween-pro-32416) <br/>

### Concepst And Categories
- Decide what category your target scene will be in. There are 3 category offers from the team but you can feel free either to add a new category or contribute a stage in one existing category.
1. *Calm* 
2. *Focus* 
3. *Excitement*

- Be careful not to be too similar to scenes that have been made before. <br/>
- Make sure the gameplay length is longer than 3 minutes and less than 12 minutes.
### Avoid doing these
- Don't change any ready prefabs, you can use it in your scene but never change it.
- Don't call at any time  `Application.Quit()` `SceneManager.LoadScene()` `SceneManager.LoadSceneAsync()`
- Don't delete or modify any files in the project
- Don't use coptright audios, logos , 3D models and any assets.
- Don't use canvas and UI objects.
- Disable hands and controllers.
### Configure Unity Project Settings
- Build Settings > Texture Compression : ASTC
- Switch Project to Android
-Project Settings > Player > XR Settings > Virtual Reality Supported: CLICK
Virtual Reality SDKs:  + Add Oculus
- Project Settings > Player > Other Settings > Graphics APIs : Remove Vulkan
- Project Settings > Player > Other Settings > Target API Level : API Level 23
### How To Create A New Canvas for VR ( You probably won't need to make this )
 - Create new Canvas
 - Layer : Default
 - Render Mode : WorldSpace
 - Canvas EventCamera : Assign here, CenterEyeAnchor
 - Canvas Pos X:0, Y:4, Z:0  (This may vary depending on your scene.)
 - Canvas Scale X: 0.01, Y:0.01, Z: 0.01
 - Add Canvas to OVRRaycaster.cs
 - UIHelper > LaserPointer > LineRenderer : Activate this (It may already active)
