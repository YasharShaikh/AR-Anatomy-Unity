# AR Anatomy

An educational Unity prototype that uses a Vuforia image target to show 3D anatomical models. On a supported mobile device, you can browse anatomical structures, rotate them with a swipe, and scale them with a pinch.

<img src="https://github.com/user-attachments/assets/4e2cae2b-ab05-4d5f-98bd-4d4a9d68b884" alt="AR Anatomy mobile preview" width="420">

## Run on a device

1. Open the repository root in **Unity 6000.0.43f1**. The [package manifest](Packages/manifest.json) expects a local **Vuforia Engine 11.1.3** package. Supply it if Unity reports it missing.
2. Open [AR Anatomy](Assets/Scenes/AR%20Anatomy.unity). Configure the Vuforia license and check the scene’s image target.
3. If models are missing, obtain the required [Z-Anatomy models](https://sketchfab.com/Z-Anatomy), import them into Unity, and assign them under the image target.
4. Build for a supported mobile device with camera access. Point the camera at the configured target, use the UI to switch models, swipe on the right half of the screen to rotate, and pinch to scale.

## Code tour

- [ObjectControl.cs](Assets/Scripts/ObjectControl.cs) reads Enhanced Touch input and applies rotation and bounded scaling.
- [ObjectSwitcher.cs](Assets/Scripts/ObjectSwitcher.cs) cycles through models and their labels.
- [ToggleObject.cs](Assets/Scripts/ToggleObject.cs) manages visibility for assigned objects.

See [LICENSE](LICENSE) for the repository license and the source listing for the external models’ terms.
