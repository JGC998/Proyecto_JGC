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