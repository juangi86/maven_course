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



