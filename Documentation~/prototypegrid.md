# Documentation

## Overview

Adds a shader inspired by Hammer/Source/Half-Life development textures. The shader projects a grid using triplanar projection. Materials can be inherited from the shader to specify grid colors. 

## Package contents

- 1 Texture
- 1 Shader (each for render pipelines)
- 1 Sample (each for render pipelines)
  - 3 Materials inheriting from shader
  - 2 Scenes
  - 1 Mesh

## Installation Instructions

Installing this package via the Unity package manager is the best way to install this package. There are multiple methods to install a third-party package using the package manager, the recommended one is `Install package from Git URL`. The URL for this package is `https://github.com/arwtsh/PrototypeGrid.git`. The Unity docs contains a walkthrough on how to install a package. It also contains information on [specifying a specific branch or release](https://docs.unity3d.com/6000.0/Documentation/Manual/upm-git.html#revision).

Alternatively, you can download directly from this GitHub repo and extract the .zip file into the folder `ProjectRoot/Packages/com.jjasundry.prototypegrid`. This will also allow you to edit the contents of the package.

## Requirements

Tested on Unity version 6000.0; will most likely work on older versions that support ShaderGraph, but you will need to manually port it.
Dependent on Unity ShaderGraph.

## Description of Assets

The core of this package is a shader that uses triplanar projection to create an opaque grid effect. The shader works in a way that prevents the triplanar projection from blending, except on faces perfectly 45 degrees. Materials can be made from this shader to customize the major grid line's color, the minor grid line's color, and the grid's background color.

The texture the grid's based on can be found in `Assets/Textures/PrototypeGrid.psd`. The file is a raw photoshop type, so it is not compressed and can be easily edited if you want to customize the grid. In the texture's import settings in Unity, it must be uncompressed. Otherwise the grid lines will bleed and blur together.

## Samples

Includes 3 samples, one for each render pipeline (they are identical other than that). Each sample includes 3 example materials using the shader. There is a scene showing how an environment can be whiteboxed using these materials. There is also a scene showing how the shader interacts with a mesh with lots of curves.
