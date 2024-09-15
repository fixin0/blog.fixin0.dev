
## What is Assimp?

Assimp (Open Asset Import Library) is an open-source library used for importing and converting 3D model data in different formats. It is especially useful in game development and 3D graphics applications. Assimp helps by converting model data (such as geometry, materials, animations, etc.) into a standard format, making it easier to work with the data in your application.

## How to Use Assimp in VS2022

- Install Assimp source code in https://github.com/assimp/assimp and extract to zip

- Please navigate to the "Configuration Properties" section and select "VC++ Directories." Here, you will need to add the paths to the Assimp header files and libraries in the "Include Directories" and "Library Directories" sections.

- Next, proceed to the "Linker" section. Here, you will find the "Input" section. Add "assimp.lib" to the "Additional Dependencies" list.

