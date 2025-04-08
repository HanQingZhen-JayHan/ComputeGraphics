# Work Graph Setup

### 1. My System
- Platform: Edition Windows 11 Pro(version 23H2, OS build22631.4317)
- GPU Hardware: Nvidia GeForce RTX 3090
- GPU Driver: Game Ready Driver 572.83(latest,2025.April)
- DirectX 12 Agility SDK 1.613.0(up to)
- DirectX Shader Copiler: 1.8.2502.8(latest, 2025.April)
- Platform Toolset: Visual Studio 2022(v143)
- Windows SDK: latest(10.0.22621.0)

https://devblogs.microsoft.com/directx/d3d12-work-graphs/

To check Agility SDK& Compiler: Right click the project, then select *"Manage NuGet Packages..."*, then select tab *Installed*.

### 2. Include d3d12 libraries
Right click the project , then select Properties, then Linker -> Input->Addtional Dependencies
```
d3d12.lib
dxgi.lib
d3dcompiler.lib
```

### 3. Examplers

Microsoft: D3D12helloWorkGraphs

https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HelloWorld/src/HelloWorkGraphs

AMD: HelloWorkGraphs

https://github.com/GPUOpen-LibrariesAndSDKs/WorkGraphsHelloWorkGraphs

### 4. Errors

**1."Device does not report support for work graphs"**

Solution: Following the above instructions.
          Restart computer or test it in the next day if not work right now.

**2.Failed to inintialize compiler.**

If you use Agility SDK 1.615.1, you may face this error.
Solution: downgrade to 1.613.0

**3.Cannot open file 
"*\WorkGraphsHelloWorkGraphs-main\x64\Debug\HelloWorkGraphs.exe"**

Solution: clean & rebuild the project,
          close & reopen the project if the error recurs.
