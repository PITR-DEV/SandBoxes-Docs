# sand.client

Messages related to clients.

## sand.client.create

| Index | Name     | Type                                    | Description                 |
| ----- | -------- | --------------------------------------- | --------------------------- |
| 0     | --       | [Identity Header](/networking/identity) | The identity header.        |
| 1     | steamId  | ulong                                   | The steam ID of the client. |
| 2     | username | string                                  | The username of the client. |

## sand.client.remove

| Index | Name | Type                                    | Description          |
| ----- | ---- | --------------------------------------- | -------------------- |
| 0     | --   | [Identity Header](/networking/identity) | The identity header. |

## sand.client.info

| Index | Name        | Type                                    | Description                     |
| ----- | ----------- | --------------------------------------- | ------------------------------- |
| 0     | --          | [Identity Header](/networking/identity) | The identity header.            |
| 1     | gameVersion | string                                  | The game version of the client. |
