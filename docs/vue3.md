
# Mouse Input-Mode "Raw Input"

To support mouse raw input you have to disable controls as follows:

```ts

AthenaClient.webview.ready(PAGE_NAME, MyView.ready);
AthenaClient.webview.open(PAGE_NAME, true, MyView.close);
AthenaClient.webview.focus();
AthenaClient.webview.showCursor(true);
alt.toggleGameControls(false);
alt.Player.local.isMenuOpen = true;

// Disable all controls needed for mouse raw input
disableAllControls(false);

```