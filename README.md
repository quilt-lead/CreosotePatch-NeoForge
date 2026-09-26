# CreosotePatch NeoForge

CreosotePatch is a lightweight **NeoForge** compatibility mod for Minecraft 1.21.1, not a legacy Forge mod. Inspired by the interoperability goal of the original [CreosotePatch](https://modrinth.com/mod/creosotepatch), this implementation goes further by changing Create's default treated-wood Spout recipe and adding bidirectional stonecutter conversions.

## Features

The mod provides two recipes:

* Create's default treated-wood Spout recipe is replaced so 250 mB of Immersive Engineering creosote and any vanilla plank produce one TFMG hardened plank instead.
* One TFMG hardened plank or one Immersive Engineering treated wood block can be converted into the other in a stonecutter.

The recipes do not modify fluid tags, Java code from other mods, or existing registries. The mod only supplies its own recipe data and requires the listed mods to be installed.

## Inspiration

This project is independently implemented and does not use code from the original mod. The original [CreosotePatch](https://modrinth.com/mod/creosotepatch) provided the inspiration for improving compatibility between Immersive Engineering and TFMG.

## Requirements

* Minecraft 1.21.1
* NeoForge 21.1.x (Forge is not supported)
* Java 21
* Create 6.0.10 or newer
* Immersive Engineering 12.4.2 or newer
* Create: The Factory Must Grow 1.2.0 or newer

## Development

This project uses Gradle and NeoGradle. To build the mod locally:

```text
.\gradlew.bat build
```

To build and launch the development client from VS Code, select **Minecraft Client** in Run and Debug. The launch configuration builds the project first and then runs the NeoForge client with the local dependency jars in `run/client/mods`.

The local dependency jars are runtime-only files and are ignored by Git.

## Releases

The GitHub Actions workflow builds releases from `v*` tags. It can also be started manually from the Actions page by providing a release tag such as `v1.0.1`. The workflow builds the mod and attaches the jar from `build/libs` to the GitHub release.

## License

This project is released under the MIT License.
