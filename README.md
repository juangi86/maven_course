# maven_course

## Market Share

- **Maven** has ~70% of the build tool market for Java applications.
- ~20% of market share: **Gradle**
- ~10% of market share: **Ant**

## Quick Project Setup

Maven brings conventions over configuration, thus reducing setup time.

## Conventions Over Configuration

**"Conventions over configuration"** (convenciones sobre configuración) es un principio de diseño que sugiere que un sistema debería prever configuraciones predeterminadas para la mayoría de las situaciones, permitiendo a los desarrolladores seguir una serie de convenciones preestablecidas en lugar de tener que configurar explícitamente cada aspecto del sistema. Esto reduce la necesidad de configuraciones detalladas y personalizadas.

### Cómo Maven Aplica Este Principio

Maven aplica este principio de las siguientes maneras:

- **Estructura de Proyecto Predeterminada**: Maven define una estructura estándar de directorios para los proyectos. Si sigues esta estructura, Maven "sabe" dónde buscar tus archivos de código fuente, recursos, archivos de configuración, etc., sin necesidad de configuración adicional.
  - `src/main/java`: Código fuente principal.
  - `src/test/java`: Código fuente de pruebas.
  - `src/main/resources`: Recursos para el código principal.
  - `src/test/resources`: Recursos para las pruebas.
 
    
## Apache Maven has stablished ‘standards’ used by other build tools

• **Maven Standard Directory Layout** - In most part adapted by other tools such as Gradle
• **Artifact Naming** - Apache Maven helped establish how Java artifacts are named.
• **Artifact Repositories** - Apache Maven established the structure of artifact repositories
• **Prior to Maven** these ‘standards’ did not exist
• **New build tools** are compatible with these ‘standards’

# Troubleshooting
![image](https://github.com/juangi86/maven_course/assets/125272484/6ff2264e-ebcd-4f27-90ca-2f232496453c)
![image](https://github.com/juangi86/maven_course/assets/125272484/9b172187-fb5d-43bc-beb1-2083a62ce9fa)



# Maven Goals

## Commonly Used Maven Goals

### 1. `clean`
   - **Description**: Removes the `target` directory, including all compiled artifacts.
   - **Command**: `mvn clean`
   - **Use Case**: Clean up the working directory by removing the build output before starting a new build.

### 2. `compile`
   - **Description**: Compiles the source code of the project.
   - **Command**: `mvn compile`
   - **Use Case**: Generate the bytecode from your source code.

### 3. `test`
   - **Description**: Runs the tests using a suitable unit testing framework.
   - **Command**: `mvn test`
   - **Use Case**: Execute the unit tests to ensure the code works as expected.

### 4. `package`
   - **Description**: Packages the compiled code into a distributable format, such as a JAR or WAR.
   - **Command**: `mvn package`
   - **Use Case**: Create a JAR/WAR file for your project that can be distributed or deployed.

### 5. `install`
   - **Description**: Installs the package into the local repository, for use as a dependency in other projects locally.
   - **Command**: `mvn install`
   - **Use Case**: Make the packaged JAR/WAR available in your local Maven repository for other projects to use as a dependency.

### 6. `deploy`
   - **Description**: Copies the final package to the remote repository for sharing with other developers and projects.
   - **Command**: `mvn deploy`
   - **Use Case**: Distribute the JAR/WAR to a remote repository for integration into other projects or for release.

### 7. `site`
   - **Description**: Generates a site based on the information in the POM.
   - **Command**: `mvn site`
   - **Use Case**: Create project documentation, reports, and a project website.

### 8. `validate`
   - **Description**: Checks if the project is correct and all necessary information is available.
   - **Command**: `mvn validate`
   - **Use Case**: Validate the project structure and configuration before building.

### 9. `verify`
   - **Description**: Runs any checks to verify the package is valid and meets quality criteria.
   - **Command**: `mvn verify`
   - **Use Case**: Perform checks and run integration tests to ensure the quality of the project.

### 10. `initialize`
   - **Description**: Initializes build state, e.g., set properties or create directories.
   - **Command**: `mvn initialize`
   - **Use Case**: Prepare the build environment and set up necessary properties.

### 11. `generate-sources`
   - **Description**: Generates any source code for inclusion in the compilation phase.
   - **Command**: `mvn generate-sources`
   - **Use Case**: Run code generation tools to produce source code before the compilation phase.

### 12. `process-sources`
   - **Description**: Processes the source code, e.g., filtering properties.
   - **Command**: `mvn process-sources`
   - **Use Case**: Apply filters and other preprocessing to the source code.

### 13. `generate-resources`
   - **Description**: Generates any resources for inclusion in the package.
   - **Command**: `mvn generate-resources`
   - **Use Case**: Create additional resources required by the project before packaging.

### 14. `process-resources`
   - **Description**: Copies and processes the resources into the output directory.
   - **Command**: `mvn process-resources`
   - **Use Case**: Handle resources (e.g., properties files) and make them ready for packaging.

### 15. `pre-clean`
   - **Description**: Executes processes needed before the `clean` phase.
   - **Command**: `mvn pre-clean`
   - **Use Case**: Prepare steps or prerequisites before the cleaning process starts.

### 16. `post-clean`
   - **Description**: Executes processes needed after the `clean` phase.
   - **Command**: `mvn post-clean`
   - **Use Case**: Perform additional steps after the cleaning process is done.

### 17. `pre-site`
   - **Description**: Executes processes needed before the `site` phase.
   - **Command**: `mvn pre-site`
   - **Use Case**: Prepare steps or prerequisites before generating the site.

### 18. `post-site`
   - **Description**: Executes processes needed after the `site` phase, and before `site-deploy`.
   - **Command**: `mvn post-site`
   - **Use Case**: Perform additional steps after the site is generated but before it is deployed.

### 19. `site-deploy`
   - **Description**: Deploys the generated site to the specified location.
   - **Command**: `mvn site-deploy`
   - **Use Case**: Upload the project website to a web server or hosting service.

     
# Maven Coordinates are used to identify artifacts

  -  Together, they identify a ‘location’ in a Maven repository.
    -  **groupId** - Typically unique to an organization. Often the organization’s reverse domain is used. But not always. Can be just ‘junit’.
    -  **artifactId** - typically the project name. A descriptor for the artifact
    -  **version** - refers to a specific version of the project.
  -  groupId and version can be inherited from a parent POM.

## Snapshots

Example 3.2.1-SNAPSHOT. Tells Maven it's a development version. Maven will first check locally, then in remote repositories. It will look in the remotes once per day.

## Maven Repositories

  - Local: <user-home>/.m2
  - Central: https://repo1.maven.org/maven2
  - Remote: Other locations

## Maven Wagon
 Set up proxies

 ![image](https://github.com/juangi86/maven_course/assets/125272484/cc6a710f-c68d-4efb-a814-1bb949f9f962)


## Maven POM

  - Must comply with maven-4.0.0.xsd
  - .xsd is an XML Schema

## Maven Lifecycles
Maven is based on the concept of build lifecycles

  - A lifecycle is a pre-defined group of build steps called **phases**
  - Each phase can be bound to one or more plugin **goals**
  - Keep in mind all work done in Maven is done by plugins!
  - Lifecycles and phases provide the framework to call plugin goals in a sequence

## Maven Archetypes
Los arquetipos de Maven son plantillas de proyectos que facilitan la creación de nuevos proyectos con una estructura y configuración predefinida. En esencia, un arquetipo de Maven es un modelo que define la estructura básica y los archivos iniciales de un proyecto, ayudándote a empezar rápidamente sin tener que configurar todo desde cero.
Ejemplo: *mvn archetype:generate -DarchetypeGroupId=org.apache.maven.archetypes -DarchetypeArtifactId=maven-archetype-simple -DarchetypeVersion=1.4*

## Maven Wrapper
Maven Wrapper es un conjunto de archivos que se añaden a un proyecto de Maven para permitir que cualquier persona pueda ejecutar Maven sin tener que instalarlo previamente en su sistema. Estos archivos aseguran que todos los desarrolladores y los entornos de integración continua (CI) usen la misma versión de Maven para construir el proyecto, eliminando problemas de compatibilidad.
  - Generar el Maven Wrapper:
    Si tu proyecto no tiene Maven Wrapper, puedes generarlo con el siguiente comando:
    mvn -N wrapper:wrapper
    Esto añadirá los archivos necesarios a tu proyecto.

  - Ejecutar comandos de Maven:
    En lugar de usar mvn, usas ./mvnw en Unix/Linux/Mac o mvnw.cmd en Windows. Por ejemplo:
    ./mvnw clean install

## Maven Global Repositories
Además de añadir repositorios en el pom.xml, también puedes configurar repositorios globales en el archivo settings.xml ubicado en el directorio ~/.m2/ (en Unix/Linux/Mac) o C:\Users\<tu-usuario>\.m2\ (en Windows). 

## Goals Example
- Build Lifecycle - CLEAN
- Has only one goal -'clean'
- Purpose is to remove files generated during build process.
- By default removes /target directory project root and submodule root folders

## Main Lifecycle Plugins

- **Clean** plugin - Build Lifecycle CLEAN - goals 'clean' (cleans resources)
- **Compiler** plugin - Build Lifecycle DEFAULT - goals 'compiler:compile', 'compiler:testCompile' 
- **Resources** plugin - Build Lifecycle DEFAULT - goals 'resources:resources', 'resources:testResources', 'resources:copy-resources' (copy project resources to an outpur directory like /target)
- **Surefire** plugin - Build Lifecycle DEFAULT - goals 'surefire:test' (Executes unit tests of the project)
- **Jar** plugin - Build Lifecycle DEFAULT - goals 'jar:jar', 'jar:test-jar' (Build jars from compiles artifacts.
- **Deploy** plugin - Build Lifecycle DEFAULT - goals 'deploy:deploy', 'deploy:deploy-file' (Deploy projecr artifacts to remote Maven repositories.
- **Site** plugin - Build Lifecycle SITE - goals 'site:site', 'site:deploy', 'site:run', 'site:stage', 'site:stage-deploy', 'site:attach-descriptor',  'site:jar', 'site:effective-site' (Hase muchas cosas nose)
