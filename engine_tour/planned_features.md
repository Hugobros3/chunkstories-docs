# Planned, envisionned and otherwise rejected features

Big projects like Chunk Stories are always playgrounds for grand idea, some of which are no-brainers, while others are more complicated to implement and will require some thinking about. Some though, sound like the person who formulated them was not equipped with a brain, making them literal no-brainers. Obviously there is no way to prevent "rejected" features from coming to life, anyone can fork Chunk Stories and make of it what they want, but for Gobrosse's sanity we'll try to tell you off doing those.

## Planned

### Full Kotlin port

Kotlin's introduction has been a very successfull experiment with the codebase and so moving forward it's only logical everything would get ported accross. Some bits of the project are tricker to port, and there is still a fair bunch of work on that front to do.

### Full survival gamemode

We're supposed to be a MC clone but so far we haven't copied it's most popular gamemode yet. Go figure.

Here is a quick list of pretty critical gameplay bricks missing:

 * Add passive mobs
 * Add (more) agressive mobs
 * Make mobs spawn automatically
 * Add/better biomes
 * Crafting and smelting systems
 * QoL/ergonomics improvements
 * Better drops on blocks and stuff
 * Better singleplayer world management (delete/rename/duplicate)
 * Better health/food mechanics (drowning etc)
 * Farming

### OpenGL / OpenGL ES 3 backend

Vulkan is nice and all but support is still spotty and lots of not-so-old hardware are entirely left out in the cold. An OpenGL ES 3 backend will function nicely as both a fallback backend and as a first step into the scary "mobile" and "not x86" world.

### Better sound

Use OpenAL EFX to enable dynamic environmental effects such as reverberation and sound muffling

 * Better footsteps
 * Environment ambient sounds ( wind, forests noises, birds, etc. )

### Enhanced launcher & bundled JVM

To avoid many tech support issues on Windows, we should just bundle an OpenJDK distribution with the launcher. This could also help with GC performance tuning. The current launcher is written in Java, but there is no reason it should absolutely be, it could be an electron app for instance. It could also use a massive improvement with regards to updating logic, and moving the authentication there may also help with security.

### Support multiple authentication methods

Provide alternatives to an account on chunkstories.xyz to log in. Possible alternative schemes:
 * Public/private key scheme, this way the user has total control over their data
 * OpenID or something
 * Steamworks (whatever you think about it, visibility is great)

### Cellular automata physics

So we can have things like fire and water with cool physics !

### Segregated / overlaid voxels for each state type ( liquid, solid )

Likes what Minecraft does, but we can take it a [lot further](https://www.reddit.com/r/VoxelGameDev/comments/9z70qc/physically_arranged_block_datalayers/?)

### Physically based rendering / Global illumination / Fancy graphics

Better lighting equations = better game ? Not sure, but GI just makes everything better.

### Less shit community platforms

In particular:
 * Make the subreddit not dead
 * A good old forum
 * A better-looking website
 * IRC-discord bridge
 * Issue tracker (not github.com)

## Envisionned

### VR

It's not really within the scope of the project and Gobrosse has no plans for it's inclusion, but there are no real blocking factors if anyone feels brave enough to hack it in.

### Mac OS X support

Even though OSX is killing it's OpenGL support and creating a Metal backend would rather go in the "rejected" bucket, we can theorically use things like MoltenVK and gfx-rs/portability as a Vulkan->Metal wrapper. This is low-priority as long as no one on the dev team has a need for it.

## Rejected

These features are very unlikely to ever make it in as they mostly go against this project technical choices and vision. Here they are so they don't get discussed to death.

### C++/Native Renderer

To put it nicely, I don't think this would work. JNI isn't very nice, and coupling two very different worlds in such a tight way over such a crappy link would be a lot of effort, a lot of overhead, a lot of ugly code and I reckon not a whole lot of performance. Vulkan nullifies most of the real problematic limitations, and CPU rendering code is therefore plenty fast, even running on the JVM.

### Lua or other forms of extra-JVM scripting

The philosphy of this project is to use the JVM for both engine code and content code, the use of a separate scripting language is something that was very deliberately avoided in this project and very much not welcome. Alternative JVM languages like Groovy or Scala are totally welcome on the other hand, as they don't require changing the entire architecture of the project. The security, complexity and performance tradeoffs of using a seperate scripting language for sandboxing user content is bound to be discussed in some blog post at some point.