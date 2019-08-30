# Content definitions & DSLs

## Design principles

One design principle that has been always at the center of attention in Chunk Stories is making it easy for the average user to discover, fiddle with and change how the content is defined. To that end we decided against defining the game content purely out of code, and instead propose a text-based, human readable format for most things.

```hjson
{
    blocks: {
        cake: {
            hardness: 0.5f
            material: slime
            textures: {
                top: cake_top
                bottom: cake_bottom
                sides: cake_sides
            }
            drops: {
                default: {
                    sugar: 1
                    chocolate: {
                        chance: 0.3
                        amount_max: 2
                    }
                }
            }
        }
    }
}
```

*An example of how the content is defined in a .hjson file*

These files use the HJSON file format, which is a superset of the well-known JSON format used everywhere in Web development these days.

## File layout

Most of the systems in the game engine that have a notion of user-created content lay out their definitions files in a named directory at the root of mods (remember, the default content is a Mod too !)

## DSLs

For some parts of the API, using a full-fledged DSL (Domain Specific Language) makes more sense. A good example is how the render graph API works. Another form of DSL is the loot definitions. Of course we can use the term DSL loosely and apply it to any definition, but here we tend to reserve the word only for describing behavior, instead of simply enumerating variants and describing them.