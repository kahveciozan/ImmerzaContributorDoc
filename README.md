# Contributor Documentation IMMERZA VR
This document is guides designers and developers to contribute to the IMMERZA VR application

Meditation App for Oculus Quest 2 
![Error](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/Immerza.png)
# What is IMMERZA
Immerza is a meditation application that aims to be published first on Applab(Sideqestvr.com) and then on Oculus Official Store.Target devices are Oculus Quest and Quest2. Currently, we have decided to consist of 3 main categories. Focus, Calm and Excitement. You can specify ideas for new category ideas. Each part should consist of 2 or 3 different parts(With different environments).

### [Immerza Website](https://www.immerza.com/)
### [Immerza Contributor Website](https://contributor.immerza.com/)

# Guidelines for Creating Content IMMERZA. Be a Contibutor.
Immerza were created using the Unity3D Game Engine

## How To Create a New Scene and Environment. (You can upload scene in 3 basic steps)
**A. Create and develop your scene in your own project. (Use Unity Version 2021.3.11.X)**  <br/>
**B. Build the scene with Addressables.**  <br/>
**C. Upload files to the website respectively.**  <br/>

### A. Creating and Development in Unity Step by Step

* Decide in which category you want to create a scene(Focus,Calm or Excitement). Then create the scene you imagine.
* Review psychology documents according to the needs of your chosen category. For Calm, For Focus, For Excitement.

1. Create Standart Unity 3D Project
2. Setting up your Project for Mobile VR
> * Files > Build Settings (Ctrl+Shift+B)
> * Select Android
> * Click the Switch Platform Button.

3. Project Setting
> * Build Settings > Texture Compression : ASTC
> * Project Settings > Player > Other Settings > Graphics APIs : Remove Vulkan
> * Project Settings > Player > Other Settings > Target API Level : API Level 23

4. Change the Camera
> * In Hierarchy, Right click > XR > Convert Main Camera To XR Rig

5. If you have import oculus sdk. Add  `OculusInteractionSampleRig.prefab` to Hierarchy. This prefab includes some particle effects(virtual breahing etc.)
6. Now you can desing your original scene. You can add our ready-mate exercises to your own scene. [Prefabs](https://www.exampleprefab.com)

### B. Built with Addressables

1. Go to Unity Package Manager and import Addressables library(Addressable Version 1.19.11.) to your unity project. This is very important to avoid problems loading the scenes.
2. Set the Group Settings ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/AddressableGroupsAndSettings.png)
3. Set the Profiles Settings ![This is an image](https://github.com/kahveciozan/ImmerzaContributorDoc/blob/main/AddressableProfiles.png)
4. ... will be update
5. Build the scene with Addressable Default Build.
6. Addressables will give 4 files (two .bundle, one json and hash file)
7. Upload these 4 files to the website respectively.

### C. Uploading .bunle files to the website
1. Go to [Immerza Contributor Website](https://contributor.immerza.com/)
2. Upload these 4 files to the website respectively.
3. Add title and descriptionon website.
4. You can update the scene whenever you want.


# Development Tools and SDKs
[Unity3D Game Engine](https://unity.com/) <br/>
[Oculus Integration SDK](https://assetstore.unity.com/packages/tools/integration/oculus-integration-82022) <br/>
[Adressable Version 1.19.11.] <br/>
[DOTween(HOTween v2)](https://assetstore.unity.com/packages/tools/visual-scripting/dotween-pro-32416) <br/>

## Requirements, Consept and Categories
- Make sure the gameplay length is longer than 3 minutes and less than 12 minutes.
-  Decide what category your target scene will be in. There are 3 category offers from the team but you can feel free either to add a new category or contribute a stage in one existing category. Consider the requirements of the category you choose. psychology documents below.
 > - [FOCUS](https://forms.gle/XvepfJQD45Uu37mT7) <br/>
 > - [CALM](https://forms.gle/XvepfJQD45Uu37mT7) <br/>
 > - [EXCITEMENT](https://forms.gle/XvepfJQD45Uu37mT7) <br/>

- [Consider the COLOUR & LIGHTING](https://forms.gle/XvepfJQD45Uu37mT7) <br/>
- [Consider the Sound & Music](https://forms.gle/XvepfJQD45Uu37mT7) <br/>
- [Consider the Mindfulness Principles](https://forms.gle/XvepfJQD45Uu37mT7) <br/>


## Avoid doing these
- Don't add any C# script. (Addressables don't support extenal code)
- Don't change any ready prefabs, you can use it in your scene but never change it.
- Don't call at any time  `Application.Quit()` `SceneManager.LoadScene()` `SceneManager.LoadSceneAsync()`
- Don't delete or modify any files in the project
- Don't use coptright audios, logos , 3D models and any assets.
- Don't use canvas and UI objects.
- Disable hands and controllers.


