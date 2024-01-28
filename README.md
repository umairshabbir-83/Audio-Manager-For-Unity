# Audio 🔉 Manager For Unity

## Usage

### Import

Import the package to the Unity Project by navigating to `Assets > Import Package > Custom Package` and selecting the `AudioManager.unitypackage` file.

### Setup

Add the `AudioManager` Prefab to the scene. This Prefab contains the `AudioManager` Script and the `AudioManager` Game Object.

### Add Sounds

Add the sounds to the `AudioManager` Game Object. The `AudioManager` Script will automatically find all the sounds in the `AudioManager` Game Object and add them to the `AudioManager` Script. The `AudioSource` Component will be added to the `AudioManager` Game Object.

### Play Sounds

To play a sound, call the `Play` method of the `AudioManager` Script. The `PlaySound` method takes the name of the sound as a parameter. The name of the sound is the name of the game object that contains the sound.

#### Example

```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class MouseClick : MonoBehaviour
{
    public AudioManager audioManager;

    public void Awake()
    {
        audioManager = FindObjectOfType<AudioManager>();
    }

    public void OnMouseDown()
    {
        audioManager.Play("Mouse Clicked");
    }

    public void OnMouseUp()
    {
        audioManager.Play("Mouse Released");
    }
}
```
