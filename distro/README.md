_Packages a distribution of configs, metadata and binaries to run OpenMRS_

-----

```bash
mvn clean package
```

Output:

`target/openmrs-distro-package/openmrs-distro-package-$version.zip`

Package contents:

| File or Directory           | Description                                                                                                                                                                                                                                                                  |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `openmrs_config`            | The OpenMRS configuration, particularly including any files to be processed by the [Initializer module](https://github.com/mekomsolutions/openmrs-module-initializer). An example configuration can be found [here](https://github.com/mekomsolutions/openmrs-config-haiti). |
| `openmrs_core`              | The main OpenMRS WAR file.                                                                                                                                                                                                                                                   |
| `openmrs_module`            | The modules (OMODs) to be run in this OpenMRS instance.                                                                                                                                                                                                                      |
| `openmrs-distro.properties` | The distro.properties used to generate this package.                                                                                                                                                                                                                         |

----

### Specifying dependencies
#### OpenMRS modules
`omod`s are specified as Maven `<dependency>` in the [pom.xml](pom.xml) file.

#### OpenMRS Configuration (Initializer)
OpenMRS config can be set in [configuration/](configuration) folder

----
