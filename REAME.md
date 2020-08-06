# Introduction
This is a course to introduce a novice developer into the key concepts and needed to create a mobile AR application using Unity's ARFoundation framework. 

I specifically chose ARFoundation for two reasons. Unity is a widely used package for the creation of [VR](https://en.wikipedia.org/wiki/Virtual_reality) applications and ARFoundation allows you to build applications for IOS and Android devices.

This course is built around the way that I learn. A combination of understanding what, why, and how through doing. How is not enough for me. Just copying someone elses script and making a few changes doesn't stick and leads to a lot of trial and error.

I also don't assume you know Unity3D or C#. I won't try to make you an expert (I'm certainly not) but I will give you enough background to keep you moving and hopefully learning.

## A word about versions.
One of my fundamental frustrations with the various tutorials and demos that appear in GitHub and on Youtube is that they become outdated quickly.

As a result there are two challenges to learning. 

- One, after completing a lesson or example it doesn't work and you spend a lot of time trying to figure out why. 

- Two, I end up learning how to do things the wrong way and spend a lot of time researching the right way.

This course is likely to suffer from the same issue of quick obsolesense as all of these other courses. To their credit Unity is making frequent changes to the AR Foundation framwork and the associated AR packages. Sometimes these changes completely change "how" a feature of the sofware is used. https://en.wikipedia.org/wiki/Virtual_reality 

As a result it is important that you match the version of Unity and AR Foundation that is used here in order to get working results. Unfortunatly, that only solves problem number one. Problem number two requires that I keep the instructions and examples current with Unity. That will be more difficult and there will always be a lag between new releases and updated material. 

In order to make the course more resiliant I will try to explain `what` we are doing and `why` we are doing it so that if the `"how"` changes it will be easier for you to make the necessary adjustments. 

### Unity and Unity package versions

The current LTS version of Unity that this course is based on is ```2019.4.6f1``` . The change log for that version can be read here https://unity3d.com/unity/whats-new/2019.4.6

Examples use [*AR Foundation 4.1*](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.1/manual/index.html).

This set of examples also rely on five Unity packages:
* ARSubsystems ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arsubsystems@4.1/manual/index.html))
* ARCore XR Plugin ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arcore@4.1/manual/index.html))
* ARKit XR Plugin ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arkit@4.1/manual/index.html))
* ARKit Face Tracking ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arkit-face-tracking@4.1/manual/index.html))
* ARFoundation ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.1/manual/index.html))
                                                                                |

If you have begun reading this course it is likely that you already know a little about Unity, C#, Unity ARFoundation, and Augmented Reality. But just to be sure we start on the same page our first lesson will be about the components we will use to create and evolve our app.

# Lesson #1

## Purpose

The purpose of this lesson is to create the development environment we will use to develop our cross platform demo app.

1. Install Unity
1. Install Xcode
1. Install A
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
