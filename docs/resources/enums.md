# Enums

## FaceMode

The `FaceMode` enum defines the different modes for face rendering.

| Index | Name     | Description                                            |
| ----- | -------- | ------------------------------------------------------ |
| 0     | None     | No face is rendered.                                   |
| 1     | BuiltIn  | The face is rendered using the built-in face texture.  |
| 2     | PixelArt | The face is rendered using a custom pixel art texture. |

## ColorMode

The `ColorMode` enum defines how the face will be colored, in relation to the body color.

| Index | Name         | Description                                                                             |
| ----- | ------------ | --------------------------------------------------------------------------------------- |
| 0     | Invert       | The face color will be inverted.                                                        |
| 1     | AutoContrast | The face will automatically pick a monochrome color that contrasts with the body color. |

## LoadType

The `LoadType` enum defines the different ways in which a layer can be loaded.

| Index | Name         | Description                         |
| ----- | ------------ | ----------------------------------- |
| 0     | OnlyLoad     | The layer is only loaded.           |
| 1     | ResetAndLoad | The layer is reset and then loaded. |
