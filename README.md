# HyperShell Zed

HyperShell Zed is a theme collection for Zed. The [HyperShell desktop project][desktop] is maintained separately.

- [**Carbon**](themes/carbon.json) pairs charcoal surfaces with cool blue accents. It is based on the [HyperShell desktop palette][hypershell] and was generated with [Omazed][omazed].

## Develop locally

1. Run `zed: install dev extension` from Zed’s command palette and select this folder.
2. Open the theme selector with `Ctrl+K` followed by `Ctrl+T` on Linux and select **Carbon**.
3. Edit [the theme JSON](themes/carbon.json) in this repository. To preview changes on save, copy it to `~/.config/zed/themes/` and disable the dev extension while using that copy.

## Add a theme

Add a JSON file under `themes/` for each new theme family. Use the `themes` array in that file for variants of the same palette.

## Publish

To submit the extension to Zed’s catalog, follow [Zed’s publishing guide][publishing].

[desktop]: https://github.com/HYP3R00T/hypershell
[hypershell]: https://github.com/HYP3R00T/hypershell/tree/main/themes/carbon
[omazed]: https://github.com/aps6/omazed
[publishing]: https://zed.dev/docs/extensions/publishing/publishing-guide
