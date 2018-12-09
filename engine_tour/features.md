# Planned, envisionned and otherwise rejected features

Big projects like Chunk Stories are always playgrounds for grand idea, some of which are no-brainers, while others are more complicated to implement and will require some thinking about. Some even, seem to originate from actual brainlessness. Obviously there is no way to prevent "rejected" features from coming to life, anyone can fork Chunk Stories and make of it what they want, but for sanity sake we'll put them in a bucket with a mean label.

## Planned in the mid-term

### Full Kotlin port

Kotlin's introduction has been a very successfull experiment with the codebase and so moving forward it's only logical everything would get ported accross.|

### Enhanced launcher & bundled JVM

To avoid many tech support issues on Windows, we should instead just bundle an OpenJDK distribution with the launcher. This could also help with GC performance tuning.

### Full survival gamemode

We're supposed to be a MC clone but so far we haven't copied it's most popular gamemode yet. Go figure.

### OpenGL ES 3 backend

Vulkan is nice and all but support is still spotty and lots of not-so-old hardware are entirely left out in the cold. An OpenGL ES 3 backend will function nicely as both a fallback backend and as a first step into the scary "mobile" and "not x86" world.

### Support multiple authentication methods

Provide alternatives to an account on chunkstories.xyz to log in. Possible alternative schemes:
 * Public/private key scheme, this way the user has total control over their data
 * OpenID or something
 * Steamworks (whatever you think about it, visibility is great)

### Cellular automata physics

So we can have things like fire and water with cool physics !

### Segregated / overlaid voxels for each state type ( liquid, solid )

Likes what Minecraft does, but we can take it a [lot further](https://www.reddit.com/r/VoxelGameDev/comments/9z70qc/physically_arranged_block_datalayers/?)

### Physically based rendering

Better lighting equations

### Less shit community platforms

In particular:
 * Make the subreddit not dead
 * A good old forum
 * A better-looking website
 * IRC-discord bridge
 * Issue tracker (not github.com)

## Envisionned

### VR

It's really not within the scope of the project and Gobrosse has no plans for it's inclusion, but there are no real blocking factors if anyone feels brave enough to hack it in.

### Mac OS X support

Even though OSX is killing it's OpenGL support and creating a Metal backend would rather go in the "rejected" bucket, we can theorically use things like MoltenVK and gfx-rs/portability as a Vulkan->Metal wrapper

## Rejected

### C++/Native Renderer

You go and deal with the JNI and writing abstractions that work well within two very different computational models elsewhere please. With the lightweight Vulkan API it's just not worth the reduced GC stress and marginal CPU cycles gained.

### Lua or other forms of extra-JVM scripting

The philosphy of this project is to use the JVM for both engine code and content code, the use of a separate scripting language is something that was very deliberately avoided in this project and very much not welcome. Alternative JVM languages like Groovy or Scala are totally welcome on the other hand, as they don't require changing the entire architecture of the project. The security, complexity and performance tradeoffs of using a seperate scripting language for sandboxing user content is bound to be discussed in some blog post at some point.