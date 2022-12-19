# Sand Format

## Minimal Example

```json
{
  "format": 1,
  "name": "Flat World",
  "author": "PITR",
  "root": {
    "type": "group",
    "key": "root_group",
    "children": [
      {
        "type": "box_brush",
        "position": {
          "x": 0,
          "y": 0,
          "z": 0
        },
        "rotation": {
          "x": 0,
          "y": 0,
          "z": 0
        },
        "scale": {
          "x": 100,
          "y": 1,
          "z": 100
        }
      },
      {
        "type": "spawn_point",
        "position": {
          "x": 0,
          "y": 5,
          "z": 0
        }
      }
    ]
  }
}
```

### Breakdown

<!-- table -->

| Key    | Type          | Required | Description                                              |
| ------ | ------------- | -------- | -------------------------------------------------------- |
| format | int           | yes      | The format version of the map.                           |
| name   | string        | yes      | The full display name of the map.                        |
| author | string        | no       | The author of the map. (Displayed as "Unknown" if empty) |
| root   | World Element | yes      | The root element of the map.                             |

## World Elements

The building blocks that make up a map.

### Group

A group is a container for other elements. It can be used to organize your map or to create a hierarchy of elements.

<!-- table -->

| Key      | Type          | Required | Description                                                                            |
| -------- | ------------- | -------- | -------------------------------------------------------------------------------------- |
| type     | string        | yes      | Must be "group".                                                                       |
| key      | string        | no       | The key of the group. Can be used to reference the group, although it is not required. |
| children | World Element | yes      | The children of the group.                                                             |
| active   | bool          | no       | Whether the group is active on start. Defaults to true.                                |

### Box Brush

A box brush is a solid box that can be used to create walls, floors, ceilings, etc.

<!-- table -->

| Key      | Type    | Required | Description                                                                            |
| -------- | ------- | -------- | -------------------------------------------------------------------------------------- |
| type     | string  | yes      | Must be "box_brush".                                                                   |
| material | string  | no       | Defaults to 'generic', must be a material key from [Materials](../resources/materials) |
| position | Vector3 | yes      | The position of the box brush.                                                         |
| rotation | Vector3 | no       | The rotation of the box brush.                                                         |
| scale    | Vector3 | yes      | The scale of the box brush.                                                            |

### Spawn Point

A spawn point is a point where players will spawn when they join the game.
By default, if there are multiple spawn points, players will spawn at a random one.

If there are no spawn points, players will spawn at Vector3.zero.

<!-- table -->

| Key      | Type    | Required | Description                      |
| -------- | ------- | -------- | -------------------------------- |
| type     | string  | yes      | Must be "spawn_point".           |
| position | Vector3 | yes      | The position of the spawn point. |
