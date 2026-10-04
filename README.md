# ME Protocol

ME Protocol is a NeoForge addon project built around Applied Energistics 2. The goal is to make AE2 the center of a complete technology progression and a modpack that does not rely on other technology mods.

The project is at the initial scaffold stage. It currently contains the mod entry point and development setup; gameplay content has not been implemented yet.

## Platform

| Component | Version |
| --- | --- |
| Minecraft | 1.21.1 |
| NeoForge | 21.1.169 |
| Applied Energistics 2 | 19.2.18 |
| Java | 21 |
| Gradle Wrapper | 8.12 |

## Build and run

Use JDK 21 from the repository root:

    .\gradlew.bat build
    .\gradlew.bat runClient

The development client uses the isolated run/client directory. The runtime includes AE2 and its required GuideME library.

## License

A license has not been selected yet. No LICENSE file is provided at this stage.