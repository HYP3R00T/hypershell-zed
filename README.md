# HyperShell Zed

HyperShell Zed is a theme collection for Zed. The [HyperShell desktop project][desktop] is maintained separately.

- [**Carbon**](themes/carbon.json) pairs charcoal surfaces with cool blue accents. Its colors come from the [HyperShell Carbon palette][palette].

## Develop locally

1. Run `zed: install dev extension` from Zed’s command palette and select this folder.
2. Open the theme selector with `Ctrl+K` followed by `Ctrl+T` on Linux and select **Carbon**.
3. Edit [the theme JSON](themes/carbon.json) in this repository. To preview changes on save, copy it to `~/.config/zed/themes/` and disable the dev extension while using that copy.

## Add a theme

Add a JSON file under `themes/` for each new theme family. Use the `themes` array in that file for variants of the same palette.

## Checks

Install the project's tools with [Mise][mise] and enable pre-commit once per clone.

```sh
mise trust
mise install
mise exec -- prek install
```

Pre-commit checks staged files when you commit. GitHub CI runs the hooks across the repository.

If a formatting check fails, run `mise exec -- biome check --write .` for files Biome supports or `mise exec -- tombi format` for TOML, then stage the fixes.

Zed uses the [schema declared in each theme][theme-schema] for diagnostics and completion while you edit.

## Publish

To submit the extension to Zed’s catalog, follow [Zed’s publishing guide][publishing].

[desktop]: https://github.com/HYP3R00T/hypershell
[palette]: https://github.com/HYP3R00T/hypershell/blob/8ffa6c5a07cfd0ad0f1db209f3d06616b9a5e68c/themes/carbon/colors.toml
[publishing]: https://zed.dev/docs/extensions/publishing/publishing-guide
[theme-schema]: https://zed.dev/schema/themes/v0.2.0.json
[mise]: https://mise.jdx.dev/getting-started.html
