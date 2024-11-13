# AR Visiting Card App
This is an Augmented Reality (AR) application developed in Unity that transforms a physical visiting card into an interactive digital experience. The app scans your visiting card using AR, and displays social media links (Instagram, GitHub, LinkedIn) as virtual floating buttons. The buttons slide in with an animated transition from the back of a virtual visiting card and provide a seamless redirect to the respective pages. Additionally, it features a rotating 3D avatar sourced from the Unity Asset Store.

# *Features*
- AR Scanning of a Visiting Card: The application uses AR technology to detect and recognize a visiting card.
- Floating Social Media Buttons: Virtual buttons appear after scanning, linking to Instagram, GitHub, and LinkedIn profiles.
- Smooth Button Animation: The social media buttons slide in from the back of the virtual card, creating an engaging animated transition.
- 3D Rotating Avatar: A 3D avatar from the Unity Asset Store rotates smoothly as part of the AR experience.
- Redirects to Social Media: Clicking on a social media button takes the user directly to the corresponding profile page.

# Getting Started
# Prerequisites
- Unity (version 2020.3 or later recommended)
- AR Foundation and ARCore/ARKit XR Plugins
- C# scripting knowledge

# Setup
- Scene Configuration: - Open the main scene, where the AR components and UI elements are set up.

- AR Camera Setup: - Ensure the AR Camera is configured with AR Session Origin and AR Session components.

- Visiting Card Detection: - Attach the AR marker recognition script to detect your visiting card. Use Unity's ARTrackedImageManager for image tracking.

- Button Animation: - The social media buttons are designed to slide in using Unity's animation system. Modify the animations or create new ones using the Animator.

- 3D Rotating Avatar: - Import the 3D avatar and place it in the scene. It is set up to rotate using a simple C# script.

# Scripts
- ButtonManager.cs: - This script handles the interaction with the social media buttons, including animations and redirects to external URLs.
- AvatarRotation.cs - This script controls the rotation of the 3D avatar.
- CardScanner.cs - Handles the AR tracking and triggers the button animations upon recognizing the visiting card.

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Linkmanager : MonoBehaviour
{
    public void openInstagram()
    {
        Application.OpenURL("https://www.instagram.com/g_karthik_29/");
    }

    public void openLinkedin()
    {
        Application.OpenURL("https://www.linkedin.com/in/karthik-g-aa92041ba/");
    }

    public void openGithub()
    {
        Application.OpenURL("https://github.com/gkarthik29");
    }

    public void opendiscord()
    {
        Application.OpenURL("https://discord.com/users/763987596212174881");
    }
}

```
# How It Works
- Scanning the Card - When the app detects the visiting card using AR, it triggers the display of virtual elements.
- Button Animation and Interaction - The social media buttons slide in from behind the virtual visiting card with an animated transition.
- 3D Avatar - The rotating 3D avatar provides a dynamic and engaging experience.

# Prerequisites
- Unity (2020.3 or newer recommended)
- AR Foundation and ARCore/ARKit XR Plugins installed
- Basic familiarity with C# scripting in Unity

# Scripts Used
**Linkmanager.cs**
- The Linkmanager script handles opening social media links when the corresponding button is clicked. It uses Application.OpenURL to open a URL in the system's default web browser.
```bash
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Linkmanager : MonoBehaviour
{
    public void openInstagram()
    {
        Application.OpenURL("https://www.instagram.com/g_karthik_29/");
    }

    public void openLinkedin()
    {
        Application.OpenURL("https://www.linkedin.com/in/karthik-g-aa92041ba/");
    }

    public void openGithub()
    {
        Application.OpenURL("https://github.com/gkarthik29");
    }

    public void opendiscord()
    {
        Application.OpenURL("https://discord.com/users/763987596212174881");
    }
}
```

**AvatarRotation.cs**
```
using UnityEngine;

public class AvatarRotation : MonoBehaviour
{
    public float rotationSpeed = 30f;

    void Update()
    {
        transform.Rotate(Vector3.up, rotationSpeed * Time.deltaTime);
    }
}
```

# Usage
- Scan the Visiting Card: - Start the app and point your device's camera at your visiting card.
- Interact with Social Buttons: - Tap on any social media button to be redirected to the respective profile.
- Experience the 3D Avatar: - Enjoy the rotating avatar for added AR immersion.
