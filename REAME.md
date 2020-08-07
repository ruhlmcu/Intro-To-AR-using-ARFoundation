# Introduction
This is a course to introduce a novice developer into the key concepts needed to create a mobile AR application using Unity's ARFoundation framework. 

I specifically chose ARFoundation for two reasons. Unity is a widely used package for the creation of [VR](https://en.wikipedia.org/wiki/Virtual_reality) applications and ARFoundation allows you to build applications for IOS and Android devices.

This course is built around the way that I learn. A combination of understanding what, why, and how through doing. How is not enough for me. Just copying someone elses script and making a few changes doesn't stick and leads to a lot of trial and error.

I also don't assume you know Unity3D or C#. I won't try to make you an expert (I'm certainly not) but I will give you enough background to keep you moving and hopefully learning.

The course does not cover: 

1. Code version control of code. You may want to investigate GitHub and GitHub Desktop.
1. Magic Leap development.
1. HoloLens development.

The installation of Visual Studio Code (a development code editor) is included for convenience. Unity3D allows for the editing of C# code and other text through an external editor. I have found that Visual Studio Code integrates very well and has several convenient extensions for C#.

### A word about versions.
One of my fundamental frustrations with the various tutorials and demos that appear in GitHub and on Youtube is that they become outdated quickly.

As a result there are two challenges to learning. 

- One, after completing a lesson or example it doesn't work and you spend a lot of time trying to figure out why. 

- Two, I end up learning how to do things the wrong way and spend a lot of time researching the right way.

This course is likely to suffer from the same issue of becoming quickly obsolete as all of these other courses. To their credit Unity is making frequent changes to the AR Foundation framework and the associated AR packages. Sometimes these changes completely change "how" a feature of the software is used. https://en.wikipedia.org/wiki/Virtual_reality 

As a result it is important that you match the version of Unity and ARFoundation that is used here in order to get working results. Unfortunately, that only solves problem number one. Problem number two requires that I keep the instructions and examples current with Unity. That will be more difficult and there will always be a lag between new releases and updated material. 

In order to make the course more resilient I will try to explain `what` we are doing and `why` we are doing it so that if the `"how"` changes it will be easier for you to make the necessary adjustments. 

### Unity and Unity package versions

The current LTS version of Unity that this course is based on is ```2019.4.7f1```. The change log for that version can be read here https://unity3d.com/unity/whats-new/2019.4.7

Examples use [*AR Foundation 4.1*](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.1/manual/index.html).

### Other software versions
Xcode 
Android SDK
Visual Studio Code 

If you have begun reading this course it is likely that you already know a little about Unity, C#, Unity ARFoundation, and Augmented Reality. But just to be sure we start on the same page our first lesson will be about the components we will use to create and evolve our app.

# Lesson #1 - Build the development environment.

### Purpose

The purpose of this lesson is to create the environment we will use to develop and test our cross platform demo app.



This lesson relies on 3rd party tutorials to support the installation process rather than repeat the instructions here. This will not be a common practice in this course, however, there are excellent installation tutorials already available from the software companies
### Install Unity Hub and Unity Editor
Step one is to install the Unity Hub and Unity Editor software.
#### Why

As stated above Unity 

#### What: 

>The Unity Hub and Unity Editor are software components supplied by Unity Technologies. 

>The Unity Hub is a management tool for managing Unity Projects and installations. The Hub can manage multiple installations of the Unity Editor along with their associated components, create new Projects, and open existing Projects.

>The Unity Editor is an Interactive Development Environment (IDE) giving users the ability to create games and experiences in both 2D and 3D. In addition it provides access to Unity's scripting API using C#.

Notes:

- You will need a Unity Account to complete this task. There is a link in the instructions
- When loading the editor select version 2019.4.7f1

[Select this link](https://docs.unity3d.com/Manual/GettingStartedInstallingHub.html) and follow the instructions on the Unity Manual page for installing the Unity Hub and the Unity Editor.   


### Install Xcode

1. [Select this link](https://developer.apple.com/download/release/) and follow the instructions on the Unity Manual page for installing the Unity Hub. 

### Install Android SDK

1. [Select this link](https://docs.unity3d.com/Manual/GettingStartedInstallingHub.html) and follow the instructions on the Unity Manual page for installing the Unity Hub. 

### Install Visual Studio Code

1. [Select this link](https://docs.unity3d.com/Manual/GettingStartedInstallingHub.html) and follow the instructions on the Unity Manual page for installing the Unity Hub. 

# Lesson #2 Configure Unity Editor for AR Development

# ARFoundation

ARFoundation is a framework from Unity that allows a developer to create and maintain an AR app within Unity3D from single Unity Project for both Andriod and IOS from . that that depends on a package called [ARSubsystems](https://docs.unity3d.com/Packages/com.unity.xr.arsubsystems@4.1/manual/index.html). ARSubsystems defines a platform-agnostic interface for surfacing different types of AR functionality and data. The AR-related subsystems are defined in this package and use the namespace UnityEngine.XR.ARSubsystems. 

This package provides interfaces for the following subsystems:

1. [Session](https://docs.unity3d.com/Packages/com.unity.xr.arsubsystems@4.1/manual/session-subsystem.html)
1. [Raycasting]()
1. [Camera]()
1. [Plane Detection]()
1. [Depth]()
1. [Image Tracking]()
1. [Face Tracking]()
1. [Environment Probes]()
1. [Object Tracking]()
1. [Occlusion]()
1. [Meshes]()


Platform-specific implementations for these subsystems are found in [ARCore - for Android devices](https://docs.unity3d.com/Packages/com.unity.xr.arcore@4.1/manual/index.html) and [ARKit - for IOS devices](https://docs.unity3d.com/Packages/com.unity.xr.arkit@4.1/manual/index.html) packages. ARFoundation turns the AR data provided by ARSubsystems into Unity [`GameObject`s](https://docs.unity3d.com/Manual/class-GameObject.html) and [`MonoBehavour`s](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html).
