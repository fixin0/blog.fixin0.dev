Game engines undoubtedly make the work of game developers much easier. Game engines have come a long way since ID Tech 1 (Doom game engine) and are now suitable not only for producing games, but also for making projects in many subjects such as Film, Architecture, Animation.

So what kind of output do these game engines produce. I did a research for this, I foresee that this series will consist of several parts.

Firstly, let's examine the architecture of a simple game engine;

![Architecture](https://www.researchgate.net/publication/323179176/figure/fig2/AS:594109840510976@1518658232445/Detailed-game-engine-architecture.png)

The architecture in this source is a considerable general architecture, while the Render engine processes resources such as Texture, Shader, Vertex, Fragment, the Physics engine processes things like Collision Detection, Collider works, Trigger. In the Scene section, things are a little different. Graphical rendering, Technical rendering and Audio rendering works in the back. But these are not the subject of this article. 

So how do these game engines compile and build everything? Actually, there is no single answer to this. There is an approach specific to each platform. In the next sections of this article, we will make a build approach on a primitive and small game engine. In this section we will go over some technical issues.

## Assets Managment

If you have worked on a game project, or if you have worked on a SDK such as .NET, it has caught your eye. The codes we write are not compiled as they are and are presented to us in a directory. But I just wanted to test the location, why is there a file called ‘Debug’? 

The answer is asset management, resources were packaged and presented to you as such while the project was being created. 

![[output.png]]

If we want to get a build operation in an engine today, we probably hope to get such a result. In current game engines, the packaging event has been carried to a slightly more advanced level and has now extended to creating binary files. But when we look at the games made with primitive game engines, for example, when we look at the Textures folder, the textures in the game appear as they are, they can be easily changed. It can be deleted and corrupted.

## Compile Code Resources

Game engines are actually a combination of many libraries. If you are writing this game engine, this means that you will write many libraries. During the build, the libraries you write will be built as well as compiling a lot of code written by the person using the engine as scripting.

When we look at current game engines, Unity converts C# code from C# to C++ with IL2CPP. The next process is as follows in Unity Documentation. https://docs.unity3d.com/6000.0/Documentation/Manual/scripting-backends-il2cpp.html


```
How IL2CPP works

When you start a build using IL2CPP, Unity automatically performs the following steps:

1. The Roslyn C# compiler compiles your application’s C# code and any required package code to .NET DLLs (managed assemblies).
2. Unity applies managed [bytecode stripping](https://docs.unity3d.com/6000.0/Documentation/Manual/managed-code-stripping.html). This step can significantly reduce the size of a built application.
3. The IL2CPP backend converts all managed assemblies into standard C++ code.
4. The C++ compiler compiles the generated C++ code and the runtime part of IL2CPP with a native platform compiler.
5. Unity creates either an executable file or a DLL, depending on the platform you target. ````

```

Now that we have talked about engine architecture and build processes, in the next section we will create a basic game with SFML and create a backend for its build.
