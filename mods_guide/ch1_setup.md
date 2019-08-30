# Chunk Stories Content creation guide

## Chapter 1: Setting up

Before we begin, we need to make sure the necessary tools are in place on your computer. To have the best experience creating content, we strongly recommand to install some software, some of which is actually mandatory.

### Mandatory software

| Software | Reason |
| --- | --- |
| Git | Used throughout the project for version control and keeping track of changes. Learning Git is an essential skill that will be usefull in pretty much anything involving computers. For Windows users, we recommand installing the complete Git package from [here](https://git-scm.com/download/win) and using the "Git Bash" prompt whenever using console commands ( not just Git's ) |
| Java Virtual Machine | While we may bundle a JVM with the client binaries, for compiling Java code you really need to have Java on your machine. We recommand OpenJDK, binaries for windows are available [here](https://adoptopenjdk.net) |
| Text Editor | Any modding work will require text editing. Notepad will technically work, but do yourself a favor and install something nice like [Notepad++](https://notepad-plus-plus.org/) or [Visual Studio Code](https://code.visualstudio.com/)
| Archive manager | To deal with mods and jars, we recommand having a good archive manager installed on your system ( windows explorer won't do ). Don't bother cracking WinRAR, use instead the much superior [7-zip](https://www.7-zip.org/download.html).

### Recommanded software

| Software | Reason |
| --- | --- |
| [Blender](https://blender.org) | While any 3D modelling program that can output .dae or .obj would work, we recommand Blender because it's free software and we store the source files for the 3d models in the .blend format. |
| [Paint.NET](https://getpaint.net) | By far the nicest to use image editor you can get for free, handles things like transparency and dithering like a charm. |
| [Audacity](https://www.audacityteam.org/) | For sound work we typically use Audacity. We don't have strong opinions about other tool, but it's what current devs use. |
| [IntelliJ Community Edition](https://www.jetbrains.com/idea/download/) | Eclipse and IntelliJ are both excellent IDEs, but since we now use Kotlin over Java, the first-class support of it makes it *ideal*. A Kotlin language server exists for other IDEs. |

### Preparing your work environment

We advise you to create a folder to put everything in. Call it `git` or `projects`. You want to clone the `chunkstories-template` repository :

```sh
git clone https://github.com/Hugobros3/chunkstories-template <yourprojectname>
cd <yourprojectname>
```

### Renaming your mod and building it

### Video

[https://www.youtube.com/watch?v=uLigFN8id3c](https://www.youtube.com/watch?v=uLigFN8id3c)

## Appendix: Cloning the game engine and building from sources