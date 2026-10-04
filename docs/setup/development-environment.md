# Development environment

## Installed and configured

- Temurin JDK 21 is available at C:\Users\epeng\jdks\jdk-21.0.12.1+1.
- The project includes the Gradle 8.12 wrapper; a separate Gradle installation is not required.
- VS Code is available. Workspace settings select Temurin JDK 21 for Java and Gradle; the workspace recommends the Java Extension Pack and Gradle for Java.
- ModDevGradle configures NeoForge 21.1.169 and the Minecraft 1.21.1 client and server launch tasks.
- run/client and run/server keep development game files separate from the source tree's resources.
- The development runtime resolves AE2 19.2.18 and its required GuideME dependency. No other technology mods are included.

## Run from PowerShell

Set Java for this terminal session, then build:

    $env:JAVA_HOME = 'C:\Users\epeng\jdks\jdk-21.0.12.1+1'
    $env:Path = "$env:JAVA_HOME\bin;$env:Path"
    .\gradlew.bat build

Start the isolated client development instance with:

    .\gradlew.bat runClient

Gradle uses the checked-in wrapper version. These commands do not change the system-wide Java setting.

On this Windows machine, Java does not automatically use the local HTTP proxy at 127.0.0.1:7897. If dependency or game-asset downloads time out, set the proxy for the current PowerShell session before running Gradle:

    $env:JAVA_TOOL_OPTIONS = '-Dhttp.proxyHost=127.0.0.1 -Dhttp.proxyPort=7897 -Dhttps.proxyHost=127.0.0.1 -Dhttps.proxyPort=7897'