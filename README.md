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
