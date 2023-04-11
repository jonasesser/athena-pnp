# V4 to V5 Mapping/Migration

1. Copy old plugin to new plugin folder
2. Remove all missing imports (underlined red) and use replacements
3. Replacements

| V4 | V5 | Client/Server |
|:----:|:-----:|:-----:|
| ```import { AthenaClient } from '@AthenaClient/api/athena';``` | ```import * as AthenaClient from '@AthenaClient/api';```    | Client |
| ```import { Athena } from '@AthenaServer/api/athena';``` | ```import * as Athena from '@AthenaServer/api';```    | Server |
| ```KeybindController.registerKeybind()```  | ```AthenaClient.systems.hotkeys.add()```    | Client |
| ```player.data```  | ```const playerData = Athena.document.character.get(player);```    | Server |
| ```isAnyMenuOpen()```  | ```AthenaClient.webview.isAnyMenuOpen()```    | Client |
| ```WebViewController.ready```  | ```AthenaClient.webview.ready```    | Client |
| ```IVehicle```  | ```OwnedVehicle```    | Shared |
| ```import { ATHENA_EVENTS_VEHICLE } from '@AthenaShared/enums/athenaEvents';```  | ```Remov import and use new autocomplete function Athena.vehicle.events.on("vehicle-spawned",...```    | Shared |



