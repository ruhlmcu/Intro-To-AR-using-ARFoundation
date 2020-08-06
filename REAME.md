# A word about versions.
One of my fundamental frustrations with the various tutorials and demos that appear in GitHub and on Youtube is that they become outdated quickly. As a result there are two challenges to learning. 

One, after completing a lesson or example it doesn't work and you spend a lot of time trying to figure out why. 

Two, I end up learning how to do things the wrong way and spend a lot of time researching the right way.

This course is likely to suffer from the same issue of quick obsolesense 

# AR Foundation Samples

Example projects that use [*AR Foundation 4.1*](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.1/manual/index.html) and demonstrate its functionality with sample assets and components.

This set of samples relies on five Unity packages:

* ARSubsystems ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arsubsystems@4.1/manual/index.html))
* ARCore XR Plugin ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arcore@4.1/manual/index.html))
* ARKit XR Plugin ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arkit@4.1/manual/index.html))
* ARKit Face Tracking ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arkit-face-tracking@4.1/manual/index.html))
* ARFoundation ([documentation](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.1/manual/index.html))

## What version should I use?

A Unity package is either "Preview" or "Verified". The latest version of ARFoundation is usually marked as preview and may include experimental or unstable features. A "verified" package is developed targeting a specific version of Unity (though it may work with earlier version as well). All packages verified for the same version of Unity are known to work well together.

In ARFoundation, this means:

| Unity Version | ARFoundation Version |
| ------------- | -------------------- |
|    2018.4     | [1.5 (preview)](https://github.com/Unity-Technologies/arfoundation-samples/tree/1.5-preview)  |
|    2019.3     | [2.1 (verified)](https://github.com/Unity-Technologies/arfoundation-samples/tree/2.1)         |
|    2020.1     | 3.0 (verified)                                                                                |
|    2020.2     | 4.1 (preview)                                                                                 |

## ARSubsystems

ARFoundation is built on "[subsystems](https://docs.unity3d.com/2019.3/Documentation/ScriptReference/Subsystem.html)" and depends on a separate package called [ARSubsystems](https://docs.unity3d.com/Packages/com.unity.xr.arsubsystems@4.1/manual/index.html). ARSubsystems defines an interface, and the platform-specific implementations are in the [ARCore](https://docs.unity3d.com/Packages/com.unity.xr.arcore@4.1/manual/index.html) and [ARKit](https://docs.unity3d.com/Packages/com.unity.xr.arkit@4.1/manual/index.html) packages. ARFoundation turns the AR data provided by ARSubsystems into Unity `GameObject`s and `MonoBehavour`s.

The `master` branch is compatible with Unity 2019.3 and later. For 2018.4, see the [1.5-preview branch](https://github.com/Unity-Technologies/arfoundation-samples/tree/1.5-preview).

## Why is ARKit Face Tracking a separate package?

For privacy reasons, use of ARKit's face tracking feature requires additional validation in order to publish your app on the App Store. If your application binary contains certain face tracking related symbols, your app may fail validation. For this reason, we provide this feature as a separate package which must be explicitly included.

## Instructions for installing AR Foundation

1. Download the latest version of Unity 2019.3 or later.

2. Open Unity, and load the project at the root of the *arfoundation-samples* repository.

3. Open your choice of sample scene.

4. See the [AR Foundation Documentation](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@4.1/manual/index.html) for usage instructions and more information.