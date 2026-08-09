
# Installation

First install plantuml from the standard update site: https://plantuml.github.io/plantuml-eclipse/

Then build the plantuml lib with customizations

```bash
cd plantuml

export CI=true
./gradlew clean build publishToMavenLocal
```


Then build the updated PlantUML Library update site

(based on https://github.com/plantuml/plantuml-eclipse/blob/main/plantuml4eclipse/releng/net.sourceforge.plantuml.parent/README.md)

Note: To build make sure a recent version of maven is ont the PATH

```bash
cd plantuml-eclipse
./gradlew buildPlantUmlLibUpdateSite -PplantUmlVersion=1.2026.6 -PcustomVersion=dan-1.0
```


Then in eclipse add update site: `C:\dan\wk\plantuml-eclipse\plantuml-lib\net.sourceforge.plantuml.library.repository\target\repository`


