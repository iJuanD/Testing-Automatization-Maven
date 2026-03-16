# Prueba Técnica - Automatización de Pruebas Web con Serenity BDD

**Proyecto**: Automatización del flujo de registro de usuario en Advantage Online Shopping  
**Tecnologías principales**: Java 17 · Maven · JUnit 5 · Selenium WebDriver · Serenity BDD  
**Patrón de diseño**: Page Object Model (POM)  

## Descripción del proyecto

Este repositorio contiene una prueba técnica de automatización de pruebas web que valida el escenario completo de **registro de un nuevo usuario** en el sitio [Advantage Online Shopping](https://www.advantageonlineshopping.com/#/).

El objetivo principal fue utilizar:
- Uso del patrón **Page Object Model**
- Configuración de un proyecto Maven moderno
- Integración de Serenity BDD con Selenium y JUnit 5
- Manejo de esperas explícitas, localizadores robustos y generación de reportes profesionales
- Resolución de problemas reales (cambios en atributos del sitio, timing de popups, mensajes de error ambiguos)

## Características clave implementadas

- Generación dinámica y única de usuarios (timestamp + prefijo) para evitar duplicados
- Llenado completo del formulario de registro (incluyendo selección de país Colombia)
- Manejo de checkbox "I agree" y validaciones frontend/backend
- Uso de esperas inteligentes de Serenity (`waitUntilVisible`, `waitUntilClickable`, `waitUntilEnabled`)
- Scroll con JavaScript para elementos fuera de vista
- Validación final del nombre de usuario en el header (`#menuUserLink`)
- Reportes detallados con screenshots y pasos en lenguaje natural (generados por Serenity)

## Tecnologías y herramientas

- **Lenguaje**: Java 17
- **Framework de pruebas**: Serenity BDD + Selenium WebDriver
- **Patrón**: Page Object Model
- **Ejecución de tests**: JUnit 5
- **Gestión de dependencias y build**: Maven
- **Assert library**: AssertJ
- **IDE**: Eclipse
- **Navegador**: Chrome (manejo automático del driver por Serenity)


## Cómo ejecutar los tests

1. Clonar el repositorio o descomprimirlo
2. Abrir el proyecto en Eclipse o IntelliJ como proyecto Maven
3. Actualizar dependencias Maven:
   - Eclipse: Clic derecho → Maven → Update Project
   - IntelliJ: Clic derecho en pom.xml → Maven → Reload project
4. Ejecutar los tests:
   ```bash
   mvn clean verify
