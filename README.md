# SSL - 2024 - K2051

## Grupo 5

Repositorio designado para los trabajos prácticos de la asignatura **"Sintaxis y Semántica de los Lenguajes"** perteneciente a la carrera de Ingeniería en Sistemas de Información dictada en la Universidad Tecnológica Nacional Facultad Regional Buenos Aires (UTN FRBA).

- ***Docente:*** Santiago Ferreiros Cabrera

---

## Objetivos del Proyecto

El objetivo principal de este repositorio es alojar el desarrollo incremental de un compilador para el lenguaje C, abarcando desde el análisis léxico hasta el análisis semántico. A través de los distintos trabajos prácticos, se implementan las diferentes etapas de compilación utilizando herramientas como **Flex** y **Bison**, así como implementaciones manuales de autómatas.

---

## Trabajos Prácticos

El proyecto se divide en 4 etapas o Trabajos Prácticos (TP), cada uno enfocado en una fase específica del proceso de compilación:

### [TP1: Autómata Finito Determinístico](./TP1)
Implementación de un Autómata Finito Determinístico (AFD) para el reconocimiento de **constantes enteras** en lenguaje C.
- **Enfoque:** Análisis léxico manual.
- **Componentes:** Implementación en C de la lógica de transición de estados.

### [TP2: Análisis Léxico con Flex](./TP2)
Desarrollo de un analizador léxico utilizando la herramienta **Flex**.
- **Objetivo:** Reconocimiento de todas las categorías léxicas del lenguaje C (palabras reservadas, identificadores, literales, operadores, etc.).
- **Componentes:** Archivo `scanner.l` con las expresiones regulares y reglas de tokenización.

### [TP3: Análisis Sintáctico con Bison](./TP3)
Implementación del análisis sintáctico utilizando **Bison** en conjunto con Flex.
- **Objetivo:** Definir la gramática del lenguaje C y verificar la corrección sintáctica del código fuente.
- **Componentes:**
    - `parser.y`: Definición de la gramática (reglas de producción).
    - `scanner.l`: Integración con el lexer del TP2.

### [TP4: Análisis Semántico (TPI)](./TP4)
Trabajo Práctico Integrador que une las etapas anteriores y añade el análisis semántico.
- **Objetivo:** Validar reglas semánticas como declaraciones de variables, tipos de datos y ámbitos (scopes).
- **Componentes:**
    - Tabla de Símbolos.
    - Chequeos de tipos y validaciones semánticas en `parser.y` y `general.c`.

---

## Componentes Principales

- **Lexer (Scanner):** Responsable de leer el flujo de caracteres de entrada y agruparlos en tokens significativos. Implementado manualmente en TP1 y con Flex en TP2-TP4.
- **Parser:** Responsable de analizar la secuencia de tokens para determinar su estructura gramatical según las reglas del lenguaje C. Implementado con Bison.
- **Tabla de Símbolos:** Estructura de datos utilizada para almacenar información sobre los identificadores (variables, funciones) definidos en el programa fuente.
- **Gestión de Errores:** Mecanismos para detectar y reportar errores léxicos, sintácticos y semánticos al usuario.
