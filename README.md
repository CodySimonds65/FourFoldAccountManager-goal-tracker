# Goal tracker

A plugin for [FourFold Account Manager](https://github.com/CodySimonds65/FourFoldAccountManager). Set a level goal
for each account: the panel shows progress toward it, and an overlay card shows the level and the XP per hour.

It is listed on the [plugin hub](https://github.com/CodySimonds65/FourFoldAccountManager-plugin-hub), so FourFold
users install it from the plugin list: the wrench in the plugin strip, then **Plugin hub**.

## As an example

Goal tracker is also a worked example for plugin authors. It shows:

- reading accounts and XP, and redrawing on `accounts.onChanged` and `xp.onUpdated` through a queue, so that redraws
  run one after another and never overlap;
- keeping settings in `fourfold.storage`;
- filling and clearing an overlay card declared in `plugin.json`.

To start your own plugin, use the
[plugin template](https://github.com/CodySimonds65/FourFoldAccountManager-plugin-template). The API is documented in
[PLUGIN_AUTHORS.md](https://github.com/CodySimonds65/FourFoldAccountManager/blob/main/PLUGIN_AUTHORS.md).

## Run it from source

1. In FourFold, open the plugin list (the wrench in the plugin strip), switch on **Developer mode**, and press
   **Open dev plugins folder**.
2. Clone this repository into that folder.

While developer mode is on, the copy in the dev folder runs instead of the one installed from the hub.

## Types

`fourfold.d.ts` and `jsconfig.json` come from the plugin template. They give an editor autocomplete and inline
documentation for `window.fourfold`. To check the plugin from a terminal (this needs Node.js):

```bash
npx -p typescript tsc -p jsconfig.json
```

## License

[Apache 2.0](LICENSE).
