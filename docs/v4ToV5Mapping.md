# V4 to V5 Mapping/Migration

1. Copy old plugin to new plugin folder
2. Remove all missing imports (underlined red) and use replacements
3. Replacements (old -> new - without warranty)

| V4 | V5 | Client/Server |
|:----:|:-----:|:-----:|
| ```import { AthenaClient } from '@AthenaClient/api/athena';``` | ```import * as AthenaClient from '@AthenaClient/api';```    | Client |
| ```import { Athena } from '@AthenaServer/api/athena';``` | ```import * as Athena from '@AthenaServer/api';```    | Server |
| ```KeybindController.registerKeybind()```  | ```AthenaClient.systems.hotkeys.add()```    | Client |
| ```player.data```  | ```const playerData = Athena.document.character.get(player);```    | Server |
| ```isAnyMenuOpen()```  | ```AthenaClient.webview.isAnyMenuOpen()```    | Client |
| ```WebViewController.ready```  | ```AthenaClient.webview.ready```    | Client |
| ```IVehicle```  | ```OwnedVehicle```    | Shared |
| ```import { ATHENA_EVENTS_VEHICLE } from '@AthenaShared/enums/athenaEvents';```  | ```Remove import and use new autocomplete function Athena.vehicle.events.on("vehicle-spawned",...```    | Shared |
| ```Athena.vehicle.func.save```  | ```await Athena.vehicle.controls.update(```    | Shared |
| ```import { PluginSystem } from '../../../server/systems/plugins';```  | ```Remove and use Athena.systems.plugins.registerPlugin(...```    | Client |
| ```import { WheelMenu } from '../../../../client/views/wheelMenu';```  | ```Remove and use AthenaClient.systems.wheelMenu.open(...```    | Client |
| ```PluginSystem.registerPlugin(```  | ```Athena.systems.plugins.registerPlugin(```    | Server |
| ```import { playerFuncs } from '../../../../server/extensions/extPlayer';```  | ```Remove and use...```    | Server |
| ```import { InputMenu, InputOptionType } from '../../../../shared/interfaces/inputMenus';```  | ```Remove and use...```    | Server |
| ```import { PedController } from '../../../../server/streamers/ped';```  | ```Remove and use...```    | Server |
| ```playerFuncs.emit.notification```  | ```Athena.player.emit.notification```    | Server |
| ```import { ServerBlipController } from '../../../server/systems/blip';```  | ```Remove and use Athena.controllers.blip.append```    | Server |
| ```await sleep```  | ```await alt.Utils.wait(100);```    | Server |
| ```await loadModel(alt.hash(model));```  | ```Remove and use...```    | Server |
| ```AgendaSystem.set(```  | ```Athena.systems.loginFlow.add(```    | Server |
| ```import ChatController from '../../../server/systems/chat';```  | ```Remove and use... #command```    | Server |
| ```import { IWheelOptionExt } from '../../../../shared/interfaces/wheelMenu';```  | ```Remove and use...```    | Server |
| ```player.data.toolbar```  | ```Athena.player.toolbar.getAt(...)```    | Server |
| ```Athena.state.set(player, 'toolbar', player.data.toolbar);```  | ```Remove and use...```    | Server |
| ```player.data.toolbar[index].quantity -= 1;```  | ```await Athena.player.toolbar.sub(player, { dbName: item.dbName, quantity: 1, data: item.data })```    | Server |
| ``` Athena.player.sync.inventory```  | ```Remove not needed anymore!?```    | Server |
| ``` behavior: ITEM_TYPE.CAN_DROP | ITEM_TYPE.CAN_TRADE | ITEM_TYPE.IS_TOOLBAR | ITEM_TYPE.CONSUMABLE | ITEM_TYPE.SKIP_CONSUMABLE,```  | ```behavior: { canDrop: true, canTrade: true, destroyOnDrop: false, isToolbar: true },```    | Shared |


4. Details

## Changes

https://athenaframework.com/blog/posts/2023-27-3
## Examples

https://athenaframework.com/tutorials/free/top/examples
## Plugins

https://athenaframework.com/tutorials/free/making-plugins/creating-plugins
## Overrides

https://athenaframework.com/blog/posts/2023-11-3



