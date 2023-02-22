# sand.layer

Messages related to sand layers.

Sand layers work as containers, for either worlds or player creations.

## sand.layer.load

| Index | Name     | Type                                  | Description                |
| ----- | -------- | ------------------------------------- | -------------------------- |
| 0     | loadType | [LoadType](/resources/enums#loadtype) | The message to be sent.    |
| 1     | rootId   | int                                   | The root id of the layer.  |
| 2     | ownerId  | string                                | The owner id of the layer. |
| 3     | map      | SandMap                               | The layer to be loaded.    |
