# Jeffstein Theme — JetBrains Plugin

The highly anticipated Jeffstein Theme, now a proper JetBrains UI theme plugin.

This is a standalone [Theme API](https://plugins.jetbrains.com/docs/intellij/themes.html) plugin (dark,
Darcula-based) that skins both the IDE chrome and the editor. It registers as a **Theme**
(Settings → Appearance & Behavior → Appearance → Theme), not just a color scheme.

## Structure

```
src/main/resources/
  META-INF/
    plugin.xml              plugin descriptor (themeProvider)
    pluginIcon.svg          plugin logo
  themes/
    jeffstein.theme.json    theme description (UI colors)
  JeffsteinTheme.xml        editor color scheme (referenced via editorScheme)
```

`jeffstein-color-theme.json` and `icon.png` at the repo root are the original
VS Code theme / logo, kept for reference.

## Build

Requires JDK 17 or 21.

```bash
./gradlew buildPlugin        # produces build/distributions/*.zip
./gradlew runIde             # launch a sandboxed IDE with the theme installed
```

## Publish

Set a Marketplace token and run:

```bash
PUBLISH_TOKEN=<token> ./gradlew publishPlugin
```
