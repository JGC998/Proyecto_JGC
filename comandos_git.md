# Uso de Comandos Git y Conceptos de Desarrollo de Software

## 1. Reconocimiento de Elementos del Desarrollo de Software

### 1.1. Conceptos de Programa Informático y de Aplicación Informática

* **Programa Informático:** Secuencia de instrucciones escritas para realizar una tarea específica en un ordenador. Puede ser simple (un script que suma dos números) o complejo. Es la unidad básica de software ejecutable.
    * *Ejemplo:* Un script en Python para renombrar archivos, el código compilado de una función específica.

* **Aplicación Informática (Software Application):** Conjunto de programas informáticos, datos y documentación relacionados, diseñados para permitir a un usuario realizar uno o varios tipos de trabajo o funciones. Suele tener una interfaz de usuario (gráfica o de línea de comandos) y gestiona una mayor complejidad que un simple programa.
    * *Ejemplo:* Un procesador de textos (Microsoft Word), un navegador web (Chrome), un sistema de gestión de bases de datos (MySQL), un videojuego.

    *En resumen:* Una aplicación está compuesta por uno o más programas y otros elementos para ofrecer una funcionalidad completa al usuario.

### 1.2. Concepto de Lenguaje de Programación

Un **lenguaje de programación** es un lenguaje formal que proporciona un conjunto de instrucciones (sintaxis y semántica) que los humanos utilizan para escribir programas que las máquinas (ordenadores) pueden entender y ejecutar. Permite comunicar algoritmos y procesos de manera precisa.

* **Sintaxis:** Las reglas que definen cómo se escriben las instrucciones válidas en el lenguaje (gramática).
* **Semántica:** El significado de esas instrucciones y cómo se comportarán cuando se ejecuten.

*Ejemplos:* Java, Python, C++, JavaScript, SQL. Cada uno tiene sus propias reglas y se utiliza para diferentes tipos de desarrollo.

### 1.3. Tipos de Lenguajes de Programación

Los lenguajes de programación se pueden clasificar de diversas maneras. Algunas de las clasificaciones más comunes son:

* **Según el Nivel de Abstracción:**
    * **Lenguajes de Bajo Nivel:** Más cercanos al hardware del ordenador. Requieren un conocimiento detallado de la arquitectura de la máquina.
        * *Lenguaje Máquina:* Instrucciones binarias que el procesador ejecuta directamente.
        * *Lenguaje Ensamblador (Assembler):* Representación simbólica del lenguaje máquina (usa mnemónicos). Es específico de cada arquitectura.
    * **Lenguajes de Alto Nivel:** Más cercanos al lenguaje humano y más fáciles de entender y usar. Abstraen los detalles del hardware. La mayoría de los lenguajes modernos son de alto nivel.
        * *Ejemplos:* Python, Java, C++, JavaScript.

* **Según el Paradigma de Programación:** Un paradigma es un estilo o forma de programar.
    * **Imperativo:** Describe la programación en términos de una secuencia de comandos que cambian el estado del programa.
        * *Procedimental:* (Ej. C, Pascal) Organiza el código en procedimientos o funciones.
        * *Orientado a Objetos (OOP):* (Ej. Java, C++, Python) Organiza el código alrededor de "objetos", que combinan datos y comportamiento.
    * **Declarativo:** Describe *qué* resultado se desea, sin especificar *cómo* lograrlo.
        * *Funcional:* (Ej. Haskell, Lisp, Scala en parte) Trata la computación como la evaluación de funciones matemáticas.
        * *Lógico:* (Ej. Prolog) Basado en la lógica formal.
    * **Multiparadigma:** Muchos lenguajes modernos soportan múltiples paradigmas (Ej. Python, C++, JavaScript, Scala).

* **Según la Forma de Ejecución:**
    * **Compilados:** Un programa traductor (compilador) convierte todo el código fuente a código máquina (o un código intermedio) antes de su ejecución.
        * *Ejemplos:* C, C++, Go.
    * **Interpretados:** Un programa (intérprete) ejecuta las instrucciones del código fuente directamente, línea por línea, o las traduce a un código intermedio sobre la marcha.
        * *Ejemplos:* Python, JavaScript (tradicionalmente), PHP.
    * **Híbridos/Intermedios:** Se compilan a un código intermedio (bytecode) que luego es ejecutado por una máquina virtual.
        * *Ejemplos:* Java (compila a bytecode, ejecutado por la JVM), C# (compila a CIL, ejecutado por el CLR).

### 1.4. Características de los Lenguajes Más Difundidos

* **Java:**
    * Orientado a objetos, fuertemente tipado.
    * Multiparadigma (principalmente OOP).
    * Compilado a bytecode ("escribe una vez, ejecuta en cualquier lugar" - WORA) y ejecutado en la Java Virtual Machine (JVM).
    * Amplio ecosistema de librerías y frameworks.
    * Usado en desarrollo empresarial, aplicaciones Android, sistemas embebidos, Big Data.
    * *Características destacadas:* Portabilidad (gracias a la JVM), gestión automática de memoria (recolector de basura), robustez.

* **Python:**
    * Interpretado (o compilado a bytecode al vuelo), tipado dinámico, multiparadigma (OOP, imperativo, funcional).
    * Sintaxis clara y legible, fácil de aprender.
    * Extensa biblioteca estándar y gran cantidad de paquetes de terceros.
    * Usado en desarrollo web (Django, Flask), ciencia de datos, machine learning, scripting, automatización.
    * *Características destacadas:* Legibilidad, productividad, gran comunidad.

* **JavaScript:**
    * Lenguaje de scripting, interpretado (los motores modernos realizan compilación JIT), multiparadigma (prototipos, funcional, imperativo).
    * Fundamental para el desarrollo web front-end (interactividad en navegadores).
    * Con Node.js, también se usa en el back-end.
    * Tipado dinámico (TypeScript añade tipado estático opcional).
    * *Características destacadas:* Asincronía, manipulación del DOM, omnipresente en la web.

* **C++:**
    * Extensión de C, multiparadigma (procedimental, OOP, genérico), compilado.
    * Permite un control de bajo nivel del hardware y gestión manual de memoria.
    * Rendimiento muy alto.
    * Usado en desarrollo de sistemas operativos, videojuegos, navegadores, aplicaciones de alto rendimiento.
    * *Características destacadas:* Rendimiento, control, complejidad.

* **C# (C Sharp):**
    * Desarrollado por Microsoft, multiparadigma (OOP, funcional, imperativo), fuertemente tipado.
    * Compilado a Common Intermediate Language (CIL) y ejecutado en el Common Language Runtime (CLR) (parte de .NET).
    * Similar a Java en muchos aspectos.
    * Usado en aplicaciones Windows, desarrollo web (ASP.NET), videojuegos (Unity).
    * *Características destacadas:* Integración con ecosistema .NET, herramientas de desarrollo (Visual Studio).

* **SQL (Structured Query Language):**
    * Lenguaje declarativo diseñado para gestionar y consultar datos en bases de datos relacionales.
    * No es un lenguaje de programación de propósito general, sino específico de dominio.
    * *Características destacadas:* Estándar para bases de datos relacionales, potente para consultas de datos.

### 1.5. Código Fuente, Código Objeto y Código Ejecutable; Máquinas Virtuales

* **Código Fuente (Source Code):**
    * Es el conjunto de instrucciones escritas por un programador en un lenguaje de programación de alto nivel (como Java, Python, C++) o de bajo nivel (como Ensamblador).
    * Es legible y comprensible para los humanos (con conocimiento del lenguaje).
    * No puede ser ejecutado directamente por la CPU en su forma original (excepto en lenguajes puramente interpretados, donde el intérprete lo procesa al vuelo).
    * *Ejemplo:* Un archivo `.java`, `.py`, `.cpp`.

* **Código Objeto (Object Code):**
    * Resultado de compilar el código fuente. Es una representación intermedia del programa en lenguaje máquina o en un formato cercano (como bytecode).
    * Puede estar compuesto por instrucciones de máquina, pero a menudo necesita ser enlazado con otras piezas de código objeto (bibliotecas) para formar un programa completo.
    * No siempre es directamente ejecutable por sí mismo.
    * *Ejemplo:* Archivos `.o` o `.obj` generados por compiladores de C/C++, archivos `.class` en Java (que contienen bytecode).

* **Código Ejecutable (Executable Code):**
    * Es la versión final de un programa que la CPU del ordenador puede ejecutar directamente (en el caso de lenguajes compilados a nativo) o que una máquina virtual puede interpretar y ejecutar (en el caso de bytecode).
    * Contiene todas las instrucciones de máquina necesarias y referencias a recursos del sistema.
    * *Ejemplo:* Un archivo `.exe` en Windows, un binario sin extensión en Linux/macOS, o el bytecode que ejecuta la JVM.

* **Máquinas Virtuales (Virtual Machines - VM):**
    * Es un software que crea un entorno de ejecución abstracto, simulando una plataforma de hardware.
    * Permiten que el mismo código compilado (generalmente bytecode) se ejecute en diferentes sistemas operativos y arquitecturas de hardware sin necesidad de recompilar el código fuente para cada plataforma.
    * Proporcionan una capa de abstracción entre el programa y el sistema operativo/hardware subyacente.
    * *Ejemplos:*
        * **JVM (Java Virtual Machine):** Ejecuta bytecode Java. Permite la portabilidad de las aplicaciones Java ("Write Once, Run Anywhere").
        * **CLR (Common Language Runtime):** Parte de .NET Framework, ejecuta CIL (Common Intermediate Language) generado a partir de C#, VB.NET, etc.
        * Intérpretes de Python: Aunque Python es interpretado, su implementación CPython compila el código fuente a bytecode que luego es ejecutado por la máquina virtual de Python.

### 1.6. Proceso de Obtención de Código Ejecutable y Herramientas

El proceso para transformar código fuente en algo que la máquina pueda ejecutar varía según el tipo de lenguaje.

**A. Para Lenguajes Compilados (ej. C, C++):**

1.  **Preprocesamiento (Preprocessing):** (Principalmente en C/C++) El preprocesador maneja directivas (ej. `#include`, `#define`). Incluye archivos de cabecera, expande macros, etc.
2.  **Compilación (Compilation):** El compilador traduce el código fuente (preprocesado) a código ensamblador específico de la arquitectura y luego a código objeto (archivos `.o` o `.obj`). Cada archivo fuente se compila por separado.
    * **Herramienta:** Compilador (ej. GCC, Clang, MSVC).
3.  **Enlazado (Linking):** El enlazador (linker) toma uno o más archivos de código objeto y los combina con código de bibliotecas (estáticas o dinámicas) para resolver referencias entre ellos y producir un único archivo ejecutable.
    * **Herramienta:** Enlazador (Linker) (ej. `ld` en sistemas Unix, `link.exe` en Windows).

**B. Para Lenguajes con Máquina Virtual (ej. Java, C#):**

1.  **Compilación a Código Intermedio:** El compilador traduce el código fuente a un código intermedio independiente de la plataforma (bytecode para Java, CIL para C#).
    * **Herramienta:** Compilador (ej. `javac` para Java, compilador Roslyn para C#).
2.  **Ejecución por la Máquina Virtual:** En tiempo de ejecución, la Máquina Virtual (JVM, CLR) carga el bytecode/CIL. Puede interpretarlo o usar un compilador Just-In-Time (JIT) para convertirlo a código máquina nativo para una ejecución más rápida.
    * **Herramienta:** Máquina Virtual (ej. `java` para ejecutar programas Java).

**C. Para Lenguajes Interpretados (ej. Python, JavaScript tradicional):**

1.  **Lectura y Análisis:** El intérprete lee el código fuente.
2.  **Traducción/Ejecución Directa:** El intérprete traduce cada instrucción a código máquina y la ejecuta, o la ejecuta directamente. Algunos intérpretes modernos pueden compilar a bytecode internamente para optimizar la ejecución repetida de código.
    * **Herramienta:** Intérprete (ej. `python`, el motor V8 de JavaScript en Chrome/Node.js).

**Herramientas Implicadas Adicionales:**

* **Traductores de Lenguajes:**
    * **Compiladores:** Traducen un lenguaje de alto nivel a uno de más bajo nivel (código objeto o máquina).
    * **Intérpretes:** Analizan y ejecutan un programa línea por línea.
    * **Ensambladores (Assemblers):** Traducen código ensamblador a código máquina.
    * **Transpiladores (Transpilers) o Compiladores Fuente-a-Fuente:** Traducen código de un lenguaje de alto nivel a otro lenguaje de alto nivel (ej. TypeScript a JavaScript, Babel para versiones modernas de JS a versiones antiguas).

* **Depuradores (Debuggers):**
    * Son herramientas esenciales que permiten a los programadores ejecutar su código paso a paso, inspeccionar el valor de las variables, establecer puntos de interrupción (breakpoints) para detener la ejecución en ciertos puntos, y analizar el flujo del programa para identificar y corregir errores (bugs).
    * La mayoría de los IDEs integran depuradores gráficos.
    * *Ejemplos:* GDB (GNU Debugger), `pdb` para Python, depuradores integrados en IntelliJ IDEA, Eclipse, Visual Studio Code.