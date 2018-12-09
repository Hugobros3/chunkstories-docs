# Chunk Stories Documentation

Welcome to the Chunk Stories documentation! This is meant to be the number one place of interest for anyone wishing to use Chunk Stories and get involved in it's development. This documentation will try to complement the admittedly still very incomplete code documentation, not just paraphrase it but actually provide guidance and tips on how to achieve things. There is much to do and much to write about, and as this is a fairly large project sadly not everything is as nicely documented as we'd like. Be assured this is meant to be a work in progress !

## User guide

 * [How to install & run Chunk Stories](install.md)
 * [Troubleshooting, common issues and bug reports](problems.md)
 * How to create a custom server
 * How to use the Minecraft map converter

## Content creation guide

This is meant as a guide for newcommers & experienced modders wanting to tackle content creation in Chunk Stories. You can skip the bits that talk about programming if that's not what you're interested in doing !

 * How to create your first mod
 * How mods work ( assets, packaging, how multiple mods interract )
 * How to make plugins & custom classes
 * Adding new blocks
 * Creating and importing 3D models in Chunk Stories
 * Adding new items
 * Introduction to entities
 * Inputs & interactions
 * Localization
 * Custom shaders & the rendergraph system

## Tour of the game engine

The goal of this part is to roughly go over every big conceptual "part" of the engine and have a small write-up about what it's purpose is, how it achieves it and how it fits into the rest. Of course you don't have to read it sequentially, feel free to click away.

 * `null`: What's yet to be.
    * [Short-term roadmap](engine_tour/roadmap.md)
    * [Planned, envisionned and otherwise rejected features](engine_tour/planned_features.md) (mid/long-term roadmap)
 * `common`: The basics of the engine
    * World data structures: How the data is stored and kept in memory
    * Custom file formats & DSLs
    * Voxels: How custom classes work and fitting them in the engine
    * Entity traits: How we deal with complex behaviors inheritance can't model
    * Items & inventories: One of the simplers systems
    * Networking: Key ideas and current limitations
    * Physics & animation
    * World generation
 * `client` : The front-end of the game most players get to see
    * GUI: Quick overview & some gotchas
    * Sound: How to play and manage your sounds
    * Graphics
        * The API: Rendergraphs to Representations
        * The Vulkan backend
            * Ressource management
            * Virtual texturing
        * The OpenGL / GLES backend
        * Interoperating with GLSL
 * `server`: It's actually not that complicated! 
 * Minecraft world `converter`

## Trivia & misc

 * Chunk Stories history
 * Project philosophy and community guidelines
 * XolioZ
