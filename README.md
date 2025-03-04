# Skeleton for homeworks at the Computer Graphics course at BME for Windows users

The purpose of this repository is to help students to setup a development environment for those who don't want to use Visual Studio or not able to use it. This tutorial was made for Windows users. Keep in mind that the commands were tested on an Windows 11 Home so if you use an other version of Windows the experience can be different.

## Disclaimers:
- This Skeleton uses openGL 3.3 which is usually supported by most modern GPU, but make sure that it is supported by your GPU.
- You can check if your GPU support OpenGL 3.3 on these links: [Intel GPUs](https://www.intel.com/content/www/us/en/support/articles/000005524/graphics.html#primary-content), [Nvidia GPUs](https://en.wikipedia.org/wiki/List_of_Nvidia_graphics_processing_units), [AMD GPUs](https://en.wikipedia.org/wiki/List_of_AMD_graphics_processing_units).
- Make sure that you have the latest drivers for your GPU otherwise OpenGL 3.3 might not be supported. You can check which version of OpenGL supported on your machine with the following program to check of your 

## Requirements:

- C/C++ compiler, that supports C++ 17 or newer. OpenGL is a platform independent API, but since the course uses C++ and that's the usual way we will use it aswell. 
- CMake 3.10 or newer. We have to build our project from source and CMake deliver an easy solution for that problem. [What is CMake?](https://cmake.org/about/)
- OpenGL. This will be our graphics API to gain acces to the power of the GPU. [What is OpenGL?](https://www.khronos.org/api/index_2016/opengl)
- Glad. This is a OpenGL Loader Generator to access OpenGL funcitons in a modern way. (It is included in the repository, but if you want to generate it for you you can try: [Generate GLAD](https://glad.dav0d.de/))
- GLM. OpenGL Mathematics is a math library for OpenGL included in the repo aswell. (You can read more about it of you want to [here](https://github.com/g-truc/glm))
- A code editor with CMake and C/C++ support. I recommend [CLion](https://www.jetbrains.com/clion/) or [VSCode](https://code.visualstudio.com/download) with CMake and C++ extensions (Optional, but highly recommended if you use vscode).

## Congrats. You have it all. You can develop programs with OpenGL 3.3 on Winndows . 
