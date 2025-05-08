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

### 1.7. Fases del Desarrollo de una Aplicación

El desarrollo de una aplicación de software es un proceso complejo que se divide en varias fases para gestionarlo de manera organizada. Aunque existen diferentes metodologías (ej. Cascada, Ágil), la mayoría comparten un conjunto de fases fundamentales:

1.  **Análisis de Requisitos:**
    * **Objetivo:** Entender y definir qué debe hacer la aplicación. Se recopilan las necesidades de los usuarios y stakeholders.
    * **Actividades:** Reuniones con clientes/usuarios, estudio de viabilidad, definición del alcance, especificación de requisitos funcionales (qué hace el sistema) y no funcionales (cómo lo hace: rendimiento, seguridad, usabilidad).
    * **Resultado:** Documento de Especificación de Requisitos del Software (ERS).

2.  **Diseño:**
    * **Objetivo:** Definir cómo se construirá la aplicación para cumplir con los requisitos.
    * **Actividades:**
        * **Diseño Arquitectónico:** Define la estructura general del sistema, componentes principales, sus interacciones y las tecnologías a utilizar.
        * **Diseño Detallado:** Especifica los módulos individuales, algoritmos, estructuras de datos, diseño de la interfaz de usuario (UI), diseño de la base de datos.
    * **Resultado:** Documento de Diseño del Software (DDS), diagramas (UML, de flujo), prototipos.

3.  **Codificación (Implementación):**
    * **Objetivo:** Traducir el diseño a código fuente utilizando el lenguaje de programación elegido.
    * **Actividades:** Escritura del código, creación de bases de datos, integración de componentes.
    * **Resultado:** Código fuente de la aplicación.

4.  **Pruebas (Testing):**
    * **Objetivo:** Verificar que la aplicación funciona según lo especificado y detectar errores (bugs).
    * **Actividades:**
        * **Pruebas Unitarias:** Probar componentes individuales o módulos.
        * **Pruebas de Integración:** Probar la interacción entre módulos.
        * **Pruebas de Sistema:** Probar el sistema completo contra los requisitos.
        * **Pruebas de Aceptación del Usuario (UAT):** El cliente/usuario valida que la aplicación cumple sus necesidades.
    * **Resultado:** Informe de pruebas, registro de errores, versión probada de la aplicación.

5.  **Documentación:**
    * **Objetivo:** Crear la documentación necesaria para diferentes audiencias.
    * **Actividades:**
        * **Documentación Técnica:** Para desarrolladores y mantenimiento (diseño, API, comentarios en código).
        * **Manual de Usuario:** Para los usuarios finales, explicando cómo usar la aplicación.
        * **Manual de Operación/Explotación:** Para administradores del sistema.
    * **Resultado:** Manuales, guías, documentación Javadoc, etc. (Esta fase se realiza a menudo en paralelo con otras).

6.  **Despliegue (Explotación/Implantación):**
    * **Objetivo:** Poner la aplicación en producción para que los usuarios puedan utilizarla.
    * **Actividades:** Instalación en servidores, configuración del entorno, migración de datos (si es necesario), capacitación de usuarios.
    * **Resultado:** Aplicación funcionando en el entorno de producción.

7.  **Mantenimiento:**
    * **Objetivo:** Asegurar que la aplicación continúe funcionando correctamente y evolucione según las necesidades cambiantes.
    * **Actividades:**
        * **Mantenimiento Correctivo:** Corregir errores descubiertos después del despliegue.
        * **Mantenimiento Adaptativo:** Modificar la aplicación para que funcione en nuevos entornos (ej. nuevo sistema operativo, cambios en hardware).
        * **Mantenimiento Perfectivo:** Mejorar la funcionalidad existente o añadir nuevas características basadas en el feedback del usuario o nuevas necesidades.
        * **Mantenimiento Preventivo:** Realizar cambios para mejorar la mantenibilidad futura o evitar problemas.
    * **Resultado:** Nuevas versiones o parches de la aplicación.

Es importante notar que en metodologías ágiles (como Scrum o Kanban), estas fases suelen ser iterativas e incrementales, en lugar de secuenciales y estrictas. Se trabaja en ciclos cortos, entregando valor funcional al final de cada ciclo.



## 2. Uso de Herramientas CASE en el Desarrollo de Software

Las herramientas CASE (Ingeniería de Software Asistida por Ordenador) son aplicaciones diseñadas para automatizar y asistir en las diversas etapas del ciclo de vida del desarrollo de software, desde la planificación hasta el mantenimiento.

* **Objetivos Principales:**
    * **Aumentar la productividad:** Automatizando tareas repetitivas y proporcionando entornos integrados.
    * **Mejorar la calidad del software:** Facilitando la aplicación de metodologías, la detección temprana de errores y la estandarización.
    * **Reducir tiempos y costes:** Optimizando procesos y mejorando la eficiencia.
    * **Facilitar la gestión de proyectos:** Ofreciendo herramientas para la planificación, seguimiento y control.
    * **Mejorar la comunicación:** Proporcionando un lenguaje común (modelos, diagramas) y repositorios compartidos.

* **Tipos (según la fase que apoyan):**
    * **Upper CASE (U-CASE):** Enfocadas en las fases iniciales (front-end del ciclo de vida).
        * *Ejemplos de funcionalidades:* Planificación de proyectos, análisis de requisitos, modelado conceptual (entidad-relación, flujo de datos), diseño de alto nivel.
        * *Herramientas típicas:* Software de modelado UML, herramientas de gestión de requisitos.
    * **Lower CASE (L-CASE):** Enfocadas en las fases finales (back-end del ciclo de vida).
        * *Ejemplos de funcionalidades:* Generación de código, compilación, depuración, pruebas, mantenimiento, ingeniería inversa.
        * *Herramientas típicas:* IDEs, generadores de código, herramientas de testing, depuradores.
    * **Integrated CASE (I-CASE) o Toolkits:** Buscan cubrir todo el ciclo de vida, integrando funcionalidades U-CASE y L-CASE en un entorno cohesivo.

* **Funcionalidades Comunes Detalladas:**
    * **Modelado Gráfico:** Creación de diagramas UML (casos de uso, clases, secuencia, actividad, etc.), diagramas de flujo de datos (DFD), diagramas entidad-relación (ERD).
    * **Diccionario de Datos / Repositorio Central:** Almacén centralizado de metadatos del proyecto (definiciones de datos, procesos, relaciones, etc.), asegurando consistencia.
    * **Generación de Código:** Creación automática de esqueletos de código o incluso código funcional a partir de modelos o especificaciones.
    * **Ingeniería Inversa:** Proceso de analizar código existente para generar modelos o representaciones de más alto nivel.
    * **Análisis y Verificación de Modelos:** Comprobación de consistencia, completitud y corrección de los modelos.
    * **Generación de Documentación:** Creación automática de documentación técnica a partir de los modelos y la información del repositorio.

* **Ventajas:** Mayor estandarización, mejora de la calidad y consistencia, detección temprana de errores, fomento de la reutilización.
* **Desventajas:** Curva de aprendizaje pronunciada, coste (especialmente I-CASE), pueden introducir rigidez si no se adaptan bien a la metodología del equipo.

---

## 3. Diseño y Realización de Pruebas

Las pruebas son un conjunto de actividades sistemáticas para evaluar la calidad de un producto software, identificar defectos y verificar que cumple con los requisitos funcionales y no funcionales.

### 3.1. Tipos de Pruebas

* **Según el conocimiento de la estructura interna:**
    * **Pruebas de Caja Blanca (Estructurales):** Se diseñan conociendo la lógica interna del código. El objetivo es asegurar que todos los caminos, bucles y condiciones se ejecutan correctamente.
        * *Técnicas:* Cobertura de sentencias (cada línea de código se ejecuta al menos una vez), cobertura de decisiones/ramas (cada rama de una estructura de control se ejecuta), cobertura de condiciones, cobertura de caminos (todos los posibles caminos lógicos).
    * **Pruebas de Caja Negra (Funcionales o de Comportamiento):** Se diseñan basándose únicamente en la especificación de requisitos, sin conocer la implementación interna. Se prueba la funcionalidad desde la perspectiva del usuario.
        * *Técnicas:* Particiones de equivalencia (dividir entradas en grupos que deberían producir el mismo resultado), análisis de valores límite (probar en los bordes de los rangos de entrada), tablas de decisión, pruebas basadas en casos de uso, pruebas de transición de estados.
    * **Pruebas de Caja Gris:** Combinación, donde el probador tiene algún conocimiento de la estructura interna para diseñar pruebas más efectivas, pero se enfoca en la funcionalidad.

* **Según el Nivel de Prueba (progresión en el ciclo de desarrollo):**
    * **Pruebas Unitarias:** Verifican la unidad más pequeña de código (funciones, métodos, clases) de forma aislada. Suelen ser automatizadas y escritas por los desarrolladores.
    * **Pruebas de Integración:** Verifican la interfaz y la interacción entre dos o más componentes o módulos que ya han sido probados unitariamente. Buscan defectos en la "unión" de las partes.
    * **Pruebas de Sistema:** Evalúan el sistema completo e integrado contra los requisitos originales (funcionales y no funcionales). Se realizan en un entorno lo más parecido posible al de producción.
    * **Pruebas de Aceptación (UAT - User Acceptance Testing):** El cliente o usuario final valida que el sistema es "apto para su propósito" y cumple con sus necesidades de negocio.
        * *Pruebas Alpha:* Realizadas por personal interno (no los desarrolladores) en un entorno controlado por la organización desarrolladora.
        * *Pruebas Beta:* Realizadas por un grupo selecto de usuarios finales en sus propios entornos, antes del lanzamiento general.

* **Según el Objetivo Específico (pruebas no funcionales y otras):**
    * **Pruebas de Regresión:** Se ejecutan repetidamente después de cada cambio en el código (corrección de bugs, nuevas funcionalidades) para asegurar que los cambios no han afectado negativamente a funcionalidades existentes.
    * **Pruebas de Rendimiento:** Evalúan cómo se comporta el sistema en términos de capacidad de respuesta, estabilidad y escalabilidad bajo una carga de trabajo particular. Incluyen pruebas de carga, estrés, resistencia y volumen.
    * **Pruebas de Usabilidad:** Evalúan qué tan fácil, eficiente y satisfactorio es para el usuario interactuar con la aplicación.
    * **Pruebas de Seguridad:** Intentan identificar vulnerabilidades, amenazas y riesgos en el software para proteger los datos y mantener la funcionalidad.
    * **Pruebas de Instalación/Desinstalación:** Verifican que el software se puede instalar, desinstalar y actualizar correctamente en los entornos soportados.
    * **Pruebas de Compatibilidad:** Aseguran que el software funciona correctamente en diferentes configuraciones de hardware, sistemas operativos, navegadores, etc.

### 3.2. Procedimientos y Casos de Prueba

* **Procedimiento de Prueba:** Documento que describe en detalle cómo ejecutar un conjunto de pruebas. Incluye: ID, propósito, precondiciones, entorno, pasos de ejecución, datos de entrada, criterios de éxito/fracaso.
* **Caso de Prueba:** Especificación de un conjunto de entradas, condiciones de ejecución, y un resultado esperado, desarrollado para un objetivo particular, como ejercitar una ruta de programa particular o verificar el cumplimiento de un requisito específico.
    * *Atributos esenciales:* ID único, nombre/descripción, precondiciones, datos de entrada, pasos a seguir, resultado esperado, resultado real, estado (Pasa/Falla), severidad/prioridad (si falla).

### 3.3. Técnicas de Diseño de Pruebas (Detalle)

* **Cubrimiento de Código (Code Coverage):** Mide el grado en que el código fuente de un programa ha sido probado. No garantiza la ausencia de errores, pero un bajo cubrimiento es una señal de alerta.
* **Análisis de Valores Límite (BVA):** Se enfoca en los "bordes" de las particiones de equivalencia. Si una entrada es válida entre 1 y 100, se prueban valores como 0, 1, 2, 99, 100, 101.
* **Particiones de Equivalencia:** Se dividen todos los posibles datos de entrada en un número finito de "clases de equivalencia" tales que se puede asumir razonablemente que una prueba de un valor representativo de cada clase es equivalente a una prueba de cualquier otro valor de esa clase.

### 3.4. Herramientas de Depuración de Código

Los depuradores (debuggers) son herramientas software que permiten a los programadores monitorizar la ejecución de un programa, detenerla (breakpoints), examinar el estado (valores de variables, pila de llamadas) y continuar la ejecución paso a paso. Son esenciales para diagnosticar y corregir errores. La mayoría de los IDEs modernos incluyen depuradores integrados.

---

## 4. Planificación de Pruebas

Es la actividad de gestión que define la estrategia general de pruebas, los objetivos, los recursos necesarios y el cronograma. El resultado es el **Plan de Pruebas**.

* **Componentes Clave del Plan de Pruebas:**
    * **Identificador del plan y Introducción:** Propósito y resumen.
    * **Ítems a Probar:** Módulos, funcionalidades o características que serán probadas.
    * **Ítems que NO se Probarán:** Y justificación.
    * **Estrategia de Prueba:** Enfoque general, niveles de prueba, tipos de prueba, criterios de inicio y finalización para cada fase.
    * **Recursos:** Personal (roles y responsabilidades), hardware, software, herramientas de prueba.
    * **Entorno de Prueba:** Especificaciones del hardware, software y configuración de red.
    * **Cronograma:** Hitos, tareas, dependencias y estimaciones de tiempo.
    * **Entregables de Prueba:** Documentos a producir (casos de prueba, scripts, informes de errores, informe resumen).
    * **Riesgos y Contingencias:** Identificación de posibles problemas y planes para mitigarlos.

### 4.1. Pruebas Unitarias; Herramientas

* **Objetivo:** Verificar la corrección de unidades de código individuales y aisladas. Son la base de una buena estrategia de pruebas.
* **Realizadas por:** Principalmente desarrolladores, a medida que escriben el código.
* **Herramientas (Frameworks):** Proporcionan una estructura para escribir y ejecutar pruebas, y para informar resultados.
    * *Java:* JUnit (muy popular), TestNG (más funcionalidades, para pruebas más complejas).
    * *Python:* `unittest` (módulo estándar), `pytest` (sintaxis más simple, potente).
    * *JavaScript:* Jest (popular para React), Mocha (flexible), Jasmine (BDD).
    * *C#:* MSTest (integrado en Visual Studio), NUnit, xUnit.net.

### 4.2. Pruebas de Integración

* **Objetivo:** Descubrir defectos en las interfaces y en las interacciones entre componentes integrados.
* **Enfoques Comunes:**
    * **Big Bang:** Se integran todos los módulos a la vez. Puede ser difícil aislar errores.
    * **Incremental:** Se añaden módulos uno por uno o en pequeños grupos.
        * *Top-Down:* Se prueban los módulos de nivel superior primero. Se usan *Stubs* (simuladores de módulos de nivel inferior aún no integrados).
        * *Bottom-Up:* Se prueban los módulos de nivel inferior primero. Se usan *Drivers* (simuladores de módulos de nivel superior que llaman al módulo bajo prueba).
        * *Sandwich/Híbrido:* Combina Top-Down y Bottom-Up.

### 4.3. Pruebas del Sistema

* **Objetivo:** Validar el comportamiento del sistema completo contra los requisitos funcionales y no funcionales especificados.
* Se realizan en un entorno que replica lo más fielmente posible el entorno de producción.
* Considera aspectos como rendimiento, seguridad, fiabilidad del sistema en su conjunto.

### 4.4. Pruebas de Aceptación

* **Objetivo:** Confirmar que el sistema está listo para su uso operativo y cumple con los criterios de aceptación del cliente/usuario.
* A menudo implican la ejecución de escenarios de negocio del mundo real.

### 4.5. Automatización de Pruebas

* **Concepto:** Utilizar herramientas software para ejecutar casos de prueba, comparar resultados reales con esperados y generar informes, sin intervención manual directa (o con mínima).
* **Beneficios Clave:** Permite la ejecución frecuente y rápida de grandes suites de pruebas (especialmente regresión), mejora la fiabilidad de las pruebas, libera a los testers para tareas más exploratorias, esencial para CI/CD.
* **Qué Automatizar:** Pruebas repetitivas, pruebas que cubren funcionalidades críticas, pruebas de regresión, pruebas de datos intensivos, pruebas de rendimiento.
* **Herramientas Populares:**
    * *UI Web:* Selenium (estándar de facto), Cypress (moderno, enfocado en desarrollador), Playwright (Microsoft).
    * *API:* Postman (manual y automatizado), RestAssured (Java), Requests (Python).
    * *Móvil:* Appium.
    * *Integración con CI/CD:* Jenkins, GitLab CI, GitHub Actions, Azure DevOps.

---

## 5. Calidad del Software

La calidad del software es un concepto multidimensional que refleja cuán bien un producto software satisface las necesidades explícitas e implícitas de sus usuarios.

### 5.1. Normas y Certificaciones

Establecen marcos y modelos para guiar y evaluar la calidad.

* **ISO/IEC 25010 (SQuaRE - Software product Quality Requirements and Evaluation):**
    * Define un modelo de calidad del producto con ocho características principales (y sub-características):
        1.  **Adecuación Funcional:** Cumplimiento funcional, completitud funcional, corrección funcional.
        2.  **Eficiencia de Desempeño:** Comportamiento temporal, utilización de recursos, capacidad.
        3.  **Compatibilidad:** Coexistencia, interoperabilidad.
        4.  **Usabilidad:** Reconocibilidad, aprendizaje, operabilidad, protección contra errores de usuario, estética de la interfaz, accesibilidad.
        5.  **Fiabilidad:** Madurez, disponibilidad, tolerancia a fallos, recuperabilidad.
        6.  **Seguridad:** Confidencialidad, integridad, no repudio, responsabilidad (accountability), autenticidad.
        7.  **Mantenibilidad:** Modularidad, reusabilidad, analizabilidad, modificabilidad, testeabilidad.
        8.  **Portabilidad:** Adaptabilidad, instalabilidad, reemplazabilidad.
* **CMMI (Capability Maturity Model Integration):** Modelo para la mejora de procesos de desarrollo. Define niveles de madurez que indican la capacidad de una organización para desarrollar software de calidad de forma consistente.
* **ISO 9001:** Norma internacional para sistemas de gestión de la calidad, aplicable a cualquier organización, incluyendo las de desarrollo de software. Se enfoca en los procesos.

### 5.2. Medidas de Calidad del Software (Métricas)

Son mediciones cuantitativas de características del software o del proceso de desarrollo.

* **Métricas del Producto (evalúan el software en sí):**
    * *Complejidad Ciclomática (McCabe):* Mide la complejidad de un módulo contando el número de caminos linealmente independientes. Mayor complejidad puede implicar más dificultad de prueba y mantenimiento.
    * *Líneas de Código (LOC/SLOC):* Medida de tamaño. Por sí sola no indica calidad, pero se usa como denominador en otras métricas (ej. defectos/KLOC).
    * *Densidad de Defectos:* Número de defectos encontrados por unidad de tamaño (ej. KLOC) o por punto de función.
    * *Tiempo Medio Entre Fallos (MTBF):* Indicador de fiabilidad.
    * *Cobertura de Pruebas:* Porcentaje del código ejercitado por las pruebas.
    * *Métricas de Orientación a Objetos (Chidamber y Kemerer):* WMC, DIT, NOC, CBO, RFC, LCOM (para clases).
* **Métricas del Proceso (evalúan el proceso de desarrollo):**
    * *Esfuerzo (ej. horas-persona, días-persona).*
    * *Coste del proyecto.*
    * *Duración del proyecto/fase.*
    * *Número de defectos detectados por fase.*
    * *Eficiencia de eliminación de defectos (DRE - Defect Removal Efficiency).*
* **Métricas de Mantenimiento:**
    * *Tiempo Medio Para Reparar (MTTR).*
    * *Índice de Mantenibilidad.*

---

## 6. Control de Versiones

Sistema que gestiona y rastrea los cambios en archivos y directorios a lo largo del tiempo, especialmente útil en el desarrollo de software para coordinar el trabajo entre múltiples personas y mantener un historial detallado.

### 6.1. Concepto y Características

* **Concepto:** Herramienta para gestionar la evolución de un proyecto, permitiendo volver a versiones anteriores, comparar cambios y entender el desarrollo histórico.
* **Características Clave:**
    * **Historial de Cambios (Log):** Registro cronológico de todas las modificaciones, quién las hizo, cuándo y (a través de mensajes de commit) por qué.
    * **Ramificación (Branching):** Creación de líneas de desarrollo paralelas e independientes. Permite trabajar en nuevas funcionalidades, experimentos o correcciones de errores sin afectar la línea principal (ej. `main` o `master`).
    * **Fusión (Merging):** Proceso de combinar los cambios de una rama en otra. Git es especialmente bueno en esto.
    * **Etiquetado (Tagging):** Marcar puntos específicos en el historial como importantes (ej. lanzamientos de versiones como `v1.0`).
    * **Reversión de Cambios:** Capacidad de deshacer cambios específicos o volver a un estado anterior del proyecto.
    * **Trabajo Concurrente y Colaboración:** Facilita que varios desarrolladores trabajen en el mismo proyecto simultáneamente.

### 6.2. Tipos de Sistemas de Control de Versiones (VCS)

* **Locales:** Todas las versiones se guardan en la máquina local del desarrollador. Poco práctico para colaboración.
* **Centralizados (CVCS - Centralized Version Control Systems):**
    * Un único servidor central contiene todas las versiones del proyecto. Los desarrolladores obtienen copias de trabajo (checkout) y envían sus cambios (commit/check-in) al servidor.
    * *Ejemplos:* Subversion (SVN), CVS, Perforce (puede ser centralizado).
    * *Ventajas:* Administración centralizada, fácil de entender para principiantes.
    * *Desventajas:* Punto único de fallo (si el servidor cae, nadie puede colaborar o guardar versiones), la mayoría de las operaciones requieren conexión de red.
* **Distribuidos (DVCS - Distributed Version Control Systems):**
    * Cada desarrollador tiene una copia completa (un clon) del repositorio en su máquina local, incluyendo todo el historial.
    * Las operaciones como commit, branching, merging se realizan localmente. La sincronización con otros repositorios (remotos) es un paso explícito.
    * *Ejemplos:* Git, Mercurial.
    * *Ventajas:* Se puede trabajar offline, mayor velocidad para operaciones locales, no hay punto único de fallo, flujos de trabajo más flexibles.
    * *Desventajas:* Curva de aprendizaje inicial puede ser más pronunciada.

### 6.3. Herramientas

* **Git:** El estándar de facto para DVCS. Creado por Linus Torvalds. Extremadamente potente, rápido y flexible. Amplia comunidad y soporte de herramientas (GitHub, GitLab, Bitbucket).
* **Subversion (SVN):** CVCS maduro y robusto, todavía utilizado en muchos proyectos legados o en organizaciones que prefieren un modelo centralizado.
* **Mercurial (hg):** Otro DVCS popular, conocido por su simplicidad relativa comparado con Git en algunos aspectos.

### 6.4. Repositorio

* **Concepto:** El "corazón" de un VCS. Es la base de datos o estructura de directorios donde se almacenan todos los archivos del proyecto, su historial completo de versiones, metadatos (como autores, fechas, mensajes de commit) y la configuración del control de versiones.
* **Repositorio Local:** La copia del repositorio que reside en la máquina de un desarrollador. Aquí es donde se realizan la mayoría de los cambios y commits.
* **Repositorio Remoto:** Una copia del repositorio alojada en un servidor accesible por red. Sirve como punto central para la colaboración entre desarrolladores, para la integración continua y como copia de seguridad.
    * *Plataformas populares para alojar repositorios remotos Git:* GitHub, GitLab, Bitbucket, Azure Repos.

---

## 7. Elaboración de Diagramas de Clases (UML)

Los diagramas de clases son un pilar de UML (Lenguaje Unificado de Modelado). Describen la estructura estática de un sistema: las clases, sus atributos (datos), sus operaciones (comportamientos) y las relaciones entre ellas.

### 7.1. Notación de Clases

* **Representación:** Un rectángulo dividido, usualmente en tres compartimentos:
    1.  **Nombre de la Clase:** En negrita, centrado. Si es abstracta, en cursiva o con `{abstract}`.
    2.  **Atributos (Miembros de Datos):** Lista de variables de la clase.
    3.  **Operaciones (Métodos):** Lista de funciones de la clase.
* **Visibilidad de Miembros:**
    * `+` : `public` (accesible desde cualquier lugar)
    * `-` : `private` (accesible solo dentro de la propia clase)
    * `#` : `protected` (accesible dentro de la clase y sus subclases)
    * `~` : `package` (visibilidad por defecto en Java, accesible dentro del mismo paquete)
* **Formato de Atributos:** `visibilidad nombreAtributo: tipo = valorInicial {propiedades}`
    * *Ejemplo:* `- nombre: String` , `+ edad: int = 0`
* **Formato de Operaciones/Métodos:** `visibilidad nombreMetodo(parametro1: tipo1, ...): tipoDeRetorno {propiedades}`
    * *Ejemplo:* `+ calcularSalario(horas: int, tarifa: double): double` , `- validarDatos()`

### 7.2. Objetos e Instanciación

* **Objeto:** Una instancia concreta de una clase. En un diagrama, se puede representar como un rectángulo con el nombre del objeto y su clase, subrayados: `nombreObjeto: NombreClase`.
    * *Ejemplo:* `miCoche: Coche`
* **Instanciación:** Es el acto de crear un objeto a partir de una clase.

### 7.3. Relaciones entre Clases

* **Asociación:**
    * Relación estructural que indica que objetos de una clase están conectados o relacionados con objetos de otra.
    * Se representa con una línea continua entre clases.
    * Puede tener un nombre, roles en cada extremo y multiplicidad.
    * *Multiplicidad:* Indica cuántos objetos de una clase pueden relacionarse con un objeto de la otra clase (ej. `1`, `0..1` (cero o uno), `*` (cero o más), `1..*` (uno o más), `2..5`).
* **Agregación (Asociación "tiene-un"):**
    * Tipo especial de asociación que representa una relación "parte-de" o "tiene-un", donde la clase "parte" puede existir independientemente de la clase "todo".
    * Se representa con un rombo hueco en el extremo de la clase "todo".
    * *Ejemplo:* Un `Departamento` *tiene-un* `Profesor` (si el departamento se elimina, el profesor puede seguir existiendo).
* **Composición (Asociación "es-parte-de" fuerte):**
    * Forma más fuerte de agregación. La "parte" depende existencialmente del "todo"; si el "todo" se destruye, la "parte" también.
    * Se representa con un rombo relleno en el extremo de la clase "todo".
    * *Ejemplo:* Un `Coche` *es-parte-de* un `Motor` (si el coche se destruye, su motor específico también).
* **Herencia (Generalización/Especialización):**
    * Indica que una clase (subclase o clase hija) hereda propiedades (atributos y métodos) de otra clase (superclase o clase padre), y puede añadir o modificar comportamiento. Relación "es-un-tipo-de".
    * Se representa con una flecha con punta triangular hueca desde la subclase hacia la superclase.
* **Dependencia:**
    * Relación más débil. Indica que un cambio en una clase (el proveedor) puede afectar a otra clase (el cliente), pero no al revés. A menudo, una clase usa a otra como parámetro de un método o tipo de variable local.
    * Se representa con una línea discontinua con una flecha abierta apuntando al proveedor.
* **Realización (Implementación de Interfaz):**
    * Indica que una clase implementa las operaciones especificadas por una interfaz.
    * Se representa con una línea discontinua y una flecha triangular hueca desde la clase implementadora hacia la interfaz (similar a la herencia, pero para interfaces). O bien, con la notación "lollipop" para interfaces.

### 7.4. Herramientas para Elaboración y Generación

* **Software de Modelado UML:** StarUML, Visual Paradigm (edición community disponible), Lucidchart (online), draw.io (diagrams.net, gratuito online y de escritorio), Enterprise Architect (comercial, muy completo).
* **Plugins en IDEs:** Muchos IDEs como IntelliJ IDEA, Eclipse, NetBeans tienen plugins para visualizar y a veces editar diagramas de clases (a menudo mediante ingeniería inversa del código).
* **Generación de Código (Ingeniería Directa):** Algunas herramientas pueden generar esqueletos de clases (archivos `.java`, `.cs`, etc.) a partir de un diagrama de clases.
* **Generación de Diagramas (Ingeniería Inversa):** Herramientas que analizan código fuente existente para generar automáticamente un diagrama de clases.

---

## 8. Elaboración de Diagramas de Comportamiento (UML)

Estos diagramas se centran en los aspectos dinámicos de un sistema, mostrando cómo interactúan los componentes y cómo evoluciona el estado del sistema con el tiempo.

### 8.1. Tipos Principales y Campo de Aplicación

* **Diagramas de Casos de Uso:** Capturan los requisitos funcionales del sistema desde la perspectiva de los usuarios (actores). Describen "qué" hace el sistema.
* **Diagramas de Interacción:** Subconjunto que muestra el flujo de control y datos entre objetos.
    * **Diagramas de Secuencia:** Enfatizan el orden temporal de los mensajes.
    * **Diagramas de Comunicación (antes Colaboración):** Enfatizan la organización de los objetos que participan en la interacción.
    * *Diagramas de Tiempos (Timing Diagrams) y Diagramas Globales de Interacción son menos comunes.*
* **Diagramas de Máquina de Estados:** Modelan el ciclo de vida de un objeto, mostrando los estados por los que pasa y las transiciones entre ellos en respuesta a eventos.
* **Diagramas de Actividad:** Representan flujos de trabajo o procesos, mostrando la secuencia de actividades y las decisiones que se toman. Similares a los diagramas de flujo.

### 8.2. Diagramas de Casos de Uso

* **Actor:** Representa un rol que interactúa con el sistema (puede ser una persona, otro sistema o dispositivo). Se dibuja como una figura de palo ("stickman").
* **Caso de Uso:** Describe una secuencia de acciones que el sistema realiza para producir un resultado observable de valor para un actor. Se representa con un óvalo con el nombre del caso de uso dentro.
* **Relación de Comunicación (Asociación):** Línea continua que conecta un actor con un caso de uso en el que participa.
* **Relaciones entre Casos de Uso:**
    * **Inclusión (`<<include>>`):** Un caso de uso base incorpora explícitamente el comportamiento de otro caso de uso. Flecha discontinua hacia el caso de uso incluido.
    * **Extensión (`<<extend>>`):** Un caso de uso (el extensor) añade comportamiento opcional a otro caso de uso base en un punto de extensión definido. Flecha discontinua hacia el caso de uso base.
    * **Generalización:** Un caso de uso hijo hereda y especializa el comportamiento de un caso de uso padre (similar a la herencia de clases).
* **Límite del Sistema:** Un rectángulo que delimita los casos de uso pertenecientes al sistema, separándolos de los actores.

### 8.3. Diagramas de Interacción

* **Diagramas de Secuencia:**
    * Muestran la interacción entre objetos ordenada cronológicamente. Eje vertical representa el tiempo (hacia abajo).
    * **Línea de Vida del Objeto (`Lifeline`):** Línea vertical discontinua bajo un rectángulo que representa un objeto (`nombreObjeto:NombreClase`).
    * **Activación (Foco de Control):** Rectángulo estrecho y alargado sobre la línea de vida, indica el período durante el cual un objeto está ejecutando una operación.
    * **Mensaje:** Flecha horizontal entre líneas de vida.
        * *Síncrono (llamada):* Flecha con punta rellena. El emisor espera respuesta.
        * *Asíncrono (señal):* Flecha con punta abierta. El emisor no espera.
        * *Retorno:* Flecha discontinua con punta abierta (opcional si es obvio).
        * *Creación de objeto:* Flecha hacia el rectángulo del objeto.
        * *Destrucción de objeto:* Flecha hacia una 'X' en la línea de vida.
    * **Fragmentos Combinados:** Para modelar bucles (`loop`), alternativas (`alt`), opcionales (`opt`), paralelos (`par`).

* **Diagramas de Comunicación (o Colaboración):**
    * Muestran las interacciones entre objetos o partes en términos de enlaces y mensajes intercambiados. No enfatizan tanto el tiempo como la estructura de la colaboración.
    * **Objetos/Participantes:** Rectángulos.
    * **Enlaces (Links):** Líneas continuas que conectan los objetos, representan una instancia de una asociación.
    * **Mensajes:** Flechas a lo largo de los enlaces, con un número de secuencia para indicar el orden y, opcionalmente, el nombre del mensaje/método.

### 8.4. Diagramas de Máquina de Estados

* Describen los posibles estados por los que un objeto puede pasar durante su ciclo de vida, así como los eventos que causan una transición de un estado a otro y las acciones que pueden ocurrir.
* **Estado:** Condición o situación durante la vida de un objeto en la que satisface alguna condición, realiza alguna actividad o espera algún evento. Se representa con un rectángulo con bordes redondeados.
    * *Estado Inicial:* Círculo relleno pequeño.
    * *Estado Final:* Círculo relleno pequeño dentro de otro círculo.
* **Transición:** Relación entre dos estados que indica que un objeto en el primer estado realizará una acción y entrará en el segundo estado cuando ocurra un evento especificado y se cumplan ciertas condiciones. Se representa con una flecha del estado origen al estado destino.
    * `evento [condiciónGuardia] / actividad`
* **Evento:** Especificación de una ocurrencia significativa que tiene una ubicación en el tiempo y el espacio. Puede ser una señal, una llamada, el paso del tiempo o un cambio de estado.
* **Acción:** Proceso o transformación atómica (no interrumpible) que se ejecuta.
* **Actividad:** Comportamiento que se ejecuta mientras un objeto está en un estado.
