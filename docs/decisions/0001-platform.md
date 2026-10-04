# 0001: Development platform

- Status: accepted for the first prototype
- Date: 2026-10-04

## Decision

| Component | Pinned version |
| --- | --- |
| Minecraft | 1.21.1 |
| NeoForge | 21.1.169 |
| Applied Energistics 2 | 19.2.18 |
| Java | 21 |
| Gradle Wrapper | 8.12 |
| ModDevGradle | 2.0.74 |

The mod id is meprotocol; the Java package is dev.meprotocol.

## Rationale

The local AE2 source checkout is the NeoForge release 19.2.18 for Minecraft 1.21.1. Its Gradle configuration pins Java 21, NeoForge 21.1.169, ModDevGradle 2.0.74, Foojay resolver 0.9.0, and Gradle 8.12. Using the same toolchain reduces compatibility surprises while implementing the AE2 addon.

AE2's published Gradle metadata declares GuideME 21.1.1 as a runtime dependency, so Gradle resolves it with AE2. The development run should otherwise contain only NeoForge, AE2, and ME Protocol; no other technology mods are configured.

## References

- Local AE2 source: reference/ae2/1.21.1-neoforge/source
- AE2 build pins: reference/ae2/1.21.1-neoforge/source/gradle.properties
- AE2 wrapper: reference/ae2/1.21.1-neoforge/source/gradle/wrapper/gradle-wrapper.properties
- AE2 Maven metadata: org.appliedenergistics:appliedenergistics2:19.2.18

## Follow-up

The mod license is still undecided. TBD in neoforge.mods.toml is a placeholder to replace before publishing.