# sand.object

Messages related to objects.

:::info

Sending a message with -1 as the root, will request the creation of a new layer.

:::

## sand.object.update

| Index | Name    | Type         | Description                                                   |
| ----- | ------- | ------------ | ------------------------------------------------------------- |
| 0     | rootId  | int          | The root Id of the object.                                    |
| 1     | element | WorldElement | The updated element. Can also be a new element to be created. |

## sand.object.remove

| Index | Name       | Type | Description                    |
| ----- | ---------- | ---- | ------------------------------ |
| 0     | rootId     | int  | The root Id of the object.     |
| 1     | instanceId | int  | The instance Id of the object. |
