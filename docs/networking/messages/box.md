# sand.box

Messages related to boxes.

In this context, a box refers to a the client's character.

## sand.box.style

| Index | Name     | Type                                    | Description               |
| ----- | -------- | --------------------------------------- | ------------------------- |
| 0     | --       | [Identity Header](/networking/identity) | The identity header.      |
| 1     | faceMode | [FaceMode](/resources/enums#facemode)   | The face mode of the box. |

:::tip

The face mode defines what the next fields will be.

:::

> FaceMode.BuiltIn
>
> | Index | Name          | Type                                    | Description                        |
> | ----- | ------------- | --------------------------------------- | ---------------------------------- |
> | 2     | buildInFaceId | string                                  | ID of a built-in face texture.     |
> | 3     | color.r       | float                                   | Red component of the body color.   |
> | 4     | color.g       | float                                   | Green component of the body color. |
> | 5     | color.b       | float                                   | Blue component of the body color.  |
> | 6     | colorMode     | [ColorMode](/resources/enums#colormode) | The color mode.                    |

---

> FaceMode.PixelArt
>
> | Index | Name        | Type                                    | Description                         |
> | ----- | ----------- | --------------------------------------- | ----------------------------------- |
> | 2     | arrayLength | int                                     | Length of the pixel art data array. |
> | 3     | pixelFace   | byte[]                                  | Pixel art data.                     |
> | 4     | color.r     | float                                   | Red component of the body color.    |
> | 5     | color.g     | float                                   | Green component of the body color.  |
> | 6     | color.b     | float                                   | Blue component of the body color.   |
> | 7     | colorMode   | [ColorMode](/resources/enums#colormode) | The color mode.                     |

## sand.box.position

| Index | Name       | Type  | Description                            |
| ----- | ---------- | ----- | -------------------------------------- |
| 0     | position.x | float | X position coordinate.                 |
| 1     | position.y | float | Y position coordinate.                 |
| 2     | position.z | float | Z position coordinate.                 |
| 3     | rotation   | float | Rotation around the Y axis in degrees. |
| 4     | stretch    | float | Stretch factor.                        |

## sand.box.state

This state controls the indicators above the box.

| Index | Name     | Type                                    | Description                                    |
| ----- | -------- | --------------------------------------- | ---------------------------------------------- |
| 0     | --       | [Identity Header](/networking/identity) | The identity header.                           |
| 1     | isTyping | bool                                    | Whenever the player has the chat open          |
| 2     | isFlying | bool                                    | Whenever the player is currently floating      |
| 3     | isPaused | bool                                    | Whenever the player's game is currently paused |
