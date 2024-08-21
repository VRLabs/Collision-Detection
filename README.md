<div align="center">

# Collision Detection

[![Generic badge](https://img.shields.io/github/downloads/VRLabs/Collision-Detection/total?label=Downloads)](https://github.com/VRLabs/Collision-Detection/releases/latest)
[![Generic badge](https://img.shields.io/badge/License-MIT-informational.svg)](https://github.com/VRLabs/Collision-Detection/blob/main/LICENSE)
[![Generic badge](https://img.shields.io/badge/Quest-Compatible-green?logo=Meta)](https://img.shields.io/badge/Quest-Compatible-green?logo=Meta)
[![Generic badge](https://img.shields.io/badge/Unity-2022.3.22f1-lightblue?logo=Unity)](https://unity.com/releases/editor/whats-new/2022.3.22)
[![Generic badge](https://img.shields.io/badge/SDK-AvatarSDK3-lightblue.svg)](https://vrchat.com/home/download)

[![Generic badge](https://img.shields.io/discord/706913824607043605?color=%237289da&label=DISCORD&logo=Discord&style=for-the-badge)](https://discord.vrlabs.dev/)
[![Generic badge](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Fshieldsio-patreon.vercel.app%2Fapi%3Fusername%3Dvrlabs%26type%3Dpatrons&style=for-the-badge)](https://patreon.vrlabs.dev/)

A contact system to detect world collision.

![Collision](https://github.com/VRLabs/Collision-Detection/assets/76777936/11b91ef5-b2d4-413d-81b2-f857a2b4bf85)

### ⬇️ [Download Latest Version](https://github.com/VRLabs/Collision-Detection/releases/latest)


### 📦 [Add to VRChat Creator Companion](https://vrlabs.dev/packages?package=dev.vrlabs.collision-detection)

</div>

---

## How it works

* A particle dies on collision with colliders, causing contacts to stop contacting each other, causing a boolean to enable.

## Install guide

https://github.com/VRLabs/Collision-Detection/assets/76777936/f9e0b70a-c5ff-43a6-a0ad-b7a3e49f3a63

* Merge the Animator Controller ``Collision Detection FX`` to your own FX Controller, using the [Avatars 3.0 Manager](https://github.com/VRLabs/Avatars-3.0-Manager) tool.
* Drag & drop the ``Collision Detection`` prefab into the base of your Hierarchy.
* Right click and unpack the prefab, then drag & drop it onto your avatar.
* Parent Constrain it to any object in your avatars hierarchy as needed.
  * Note: You can move the object as well, but you'd have to repath the animations. One tool for this is [hfcred's Animation Repathing tool](https://github.com/hfcRed/Animation-Repathing)

> [!NOTE]  
> When building for Quest, you will have to remove unsupported components and shaders

## How to use

* After parent constraining/moving the object as needed, you can scale the object to obtain the desired range.
  * Note: To change the collision requirements, you can change the Layers in the `collision` module, or disable the `collision` module and enable the `triggers` module to select specific trigger colliders.

There are three important bools in your FX Controller:

* ``CollisionDetection/IsColliding``: Whether or not the component is currently colliding with a collider.
* ``CollisionDetection/AlwaysReset``: Whether or not IsColliding should go to false immediately after stopping collision, or stay on until the Reset bool is enabled.
* ``CollisionDetection/Reset``: If ``CollisionDetection/AlwaysReset`` is false, this bool is used to reset the IsColliding state.

## Performance stats

```c++
Contact Senders:    1
Contact Receivers:  1
FX Animator Layers: 1
Particle Systems:   1
```

## Hierarchy layout

```html
Collision Detection
```

## Contributors

* [hfcred](https://github.com/hfcred)
* [jellejurre](https://github.com/jellejurre)

## License

Collision Detection is available as-is under MIT. For more information see [LICENSE](https://github.com/VRLabs/Collision-Detection/blob/main/LICENSE).

​

<div align="center">

[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/VRLabs.png" width="50" height="50">](https://vrlabs.dev "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Discord.png" width="50" height="50">](https://discord.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Patreon.png" width="50" height="50">](https://patreon.vrlabs.dev/ "VRLabs")
<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Empty.png" width="10">
[<img src="https://github.com/VRLabs/Resources/raw/main/Icons/Twitter.png" width="50" height="50">](https://twitter.com/vrlabsdev "VRLabs")

</div>

