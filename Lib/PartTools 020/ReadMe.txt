--- PartTools 0.20 ---

UPGRADING FROM PREVIOUS EDITIONS

 If you are upgrading your existing part project to use the new PartTools you have a few steps to take.

1. First import the UpgradeProject package included in this zip
2. Run the script via the menu option Tools->Upgrade PartTools
3. Delete the old Plugins/KSP directory
4. Import the PartTools package included in the zip
5. All existing PartTools prefabs will require resetting to use the new PartTools component.


Overview

 PartTools has had a refresh and is now a lot easier to use. It comes in precompiled dlls and a nicer directory structure and supports some more advanced features. 
 Because of the ability to read another model's textures by name, it no longer forces renaming of textures to modelXXX. The 'model name' is now used as the actual filename of the model. Do not add an extension to this field.

 To make PartTools work you need to add the new package to Unity and then set your GameData directory via Tools->KSP PartTools. This will set the GameData directory and make all paths used in PartTools relative to that.



KSPParticleEmitter

 PartTools now also supports a particle emitter, KSPParticleEmitter which is included in the PartTools package. Unity native particle emitters will not work as they are not fully serializable. KSPParticleEmitter is based upon the legacy particle emitter, see the unity docs for information, however it also supports a variety of emitter shapes. 
 The KSPParticleEmitter is fully animatable via the standard unity animation system like other PartTools assets.

 To create a material for a KSPParticleEmitter use the two included KSP/Particle shaders. There is an alpha blended and additive shader.



PropTools

 PropTools, the system to create internal spaces for KSP, has had a major rebuild. It can now load and save internal space configs and also load models and textures of the props and internal spaces. No longer having to use the awful proxy system!

 If you are working on an existing internal space then open the PartTools window (Tools->KSP PartTools), set the game's GameData directory and then you can instantiate internal spaces and props via that window.

 If you are creating a new internal space then you currently need to create an INTERNAL config manually. That can then be loaded by PartTools.

 NOTE: Always keep the PartTools window open as it assists in prop selection to sidestep a Unity editor bug.