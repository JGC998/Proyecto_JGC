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

Las herramientas CASE (Ingeniería de Software Asistida por Ordenador) automatizan y simplifican fases del ciclo de vida del software.

* **Objetivos:** Mejorar productividad, calidad, reducir tiempos/costes, facilitar gestión y comunicación.
* **Tipos:**
    * **Upper CASE (U-CASE):** Primeras fases (planificación, análisis, diseño).
    * **Lower CASE (L-CASE):** Últimas fases (generación código, compilación, pruebas, mantenimiento).
    * **Integrated CASE (I-CASE):** Cubren todo el ciclo.
* **Funcionalidades:** Modelado, generación de diagramas (UML), repositorios de metadatos, generación de código, ingeniería inversa, validación, gestión de configuración, documentación.
* **Ventajas:** Estandarización, mejora calidad, detección temprana errores, reutilización.
* **Desventajas:** Curva aprendizaje, coste, posible rigidez metodológica.

---

## 3. Diseño y Realización de Pruebas

Proceso para asegurar calidad, verificar requisitos y detectar errores.

### 3.1. Tipos de Pruebas

* **Según conocimiento interno:**
    * **Caja Blanca (Estructurales):** Conoce el código. Verifica flujos internos. *Técnicas:* Cobertura de sentencias, decisiones, caminos.
    * **Caja Negra (Funcionales):** Desconoce el código. Prueba E/S según especificaciones. *Técnicas:* Particiones equivalencia, valores límite.
    * **Caja Gris:** Conocimiento parcial.
* **Según Nivel:**
    * **Unitarias:** Módulos pequeños y aislados (por desarrolladores).
    * **Integración:** Interacción entre módulos.
    * **Sistema:** Sistema completo contra requisitos.
    * **Aceptación (UAT):** Cliente valida el sistema. (Alpha: interna; Beta: externa).
* **Según Objetivo Específico:**
    * **Regresión:** Asegura que cambios no rompan lo existente.
    * **Rendimiento:** Capacidad de respuesta, estabilidad, carga.
    * **Usabilidad:** Facilidad de uso.
    * **Seguridad:** Vulnerabilidades.

### 3.2. Procedimientos y Casos de Prueba

* **Procedimiento de Prueba:** Pasos detallados para ejecutar pruebas.
* **Caso de Prueba:** Entradas, condiciones y resultados esperados para verificar un aspecto. *Componentes:* ID, descripción, precondiciones, pasos, datos entrada, resultado esperado/obtenido, estado.

### 3.3. Técnicas de Diseño de Pruebas

* **Cubrimiento de Código (Code Coverage):** (Caja blanca) % de código ejecutado por pruebas.
* **Análisis de Valores Límite (BVA):** (Caja negra) Prueba límites de rangos de entrada.
* **Particiones de Equivalencia:** (Caja negra) Divide entradas en clases; prueba un valor por clase.

### 3.4. Herramientas de Depuración de Código

Permiten ejecutar paso a paso, inspeccionar variables, puntos de interrupción, pila de llamadas. Integradas en IDEs (GDB, pdb, etc.).

---

## 4. Planificación de Pruebas

Define estrategia, objetivos, recursos y cronograma en un **Plan de Pruebas**.

* **Componentes Clave del Plan:** Alcance, estrategia, criterios entrada/salida, recursos, entorno, cronograma, entregables, riesgos.

### 4.1. Pruebas Unitarias; Herramientas

* **Objetivo:** Probar unidades aisladas. Automatizadas y rápidas.
* **Herramientas (Frameworks):** JUnit, TestNG (Java); unittest, pytest (Python); Jest, Mocha (JS); MSTest, NUnit (C#).

### 4.2. Pruebas de Integración

* **Objetivo:** Verificar interacción entre módulos.
* **Enfoques:** Big Bang (todos a la vez), Incremental (Top-Down, Bottom-Up, Sandwich).

### 4.3. Pruebas del Sistema

* **Objetivo:** Probar sistema completo en entorno similar a producción. Basadas en requisitos.

### 4.4. Pruebas de Aceptación

* **Objetivo:** Cliente valida el sistema. (UAT, Alpha, Beta).

### 4.5. Automatización de Pruebas

* **Concepto:** Usar software para ejecutar pruebas, comparar resultados y generar informes.
* **Ventajas:** Ahorro tiempo/coste, mayor cobertura, ejecución rápida/frecuente, reduce error humano, facilita CI/CD.
* **Herramientas:** Frameworks unitarios, Selenium/Cypress (UI Web), Postman/RestAssured (API), Jenkins/GitLab CI (CI/CD).

---

## 5. Calidad del Software

Grado en que un sistema cumple requisitos y expectativas.

### 5.1. Normas y Certificaciones

* **ISO/IEC 25010 (SQuaRE):** Modelo de calidad del producto software (funcionalidad, fiabilidad, usabilidad, eficiencia, mantenibilidad, portabilidad).
* **CMMI:** Modelo de madurez para mejora de procesos.
* **ISO 9001:** Sistema de gestión de calidad general.

### 5.2. Medidas de Calidad del Software (Métricas)

Medidas cuantitativas para evaluar aspectos del producto o proceso.

* **Métricas del Producto:** Complejidad ciclomática, LOC, densidad de defectos, MTBF, cobertura de pruebas.
* **Métricas del Proceso:** Esfuerzo, coste, tiempo de ciclo, defectos por fase.

---

## 6. Control de Versiones

Sistema que registra cambios en archivos a lo largo del tiempo, permitiendo recuperar versiones.

### 6.1. Concepto y Características

* **Concepto:** Gestionar evolución de archivos.
* **Características:** Historial, ramificación (branching), fusión (merging), reversión, colaboración.

### 6.2. Tipos de Sistemas de Control de Versiones (VCS)

* **Centralizados (CVCS):** Servidor único (SVN, CVS). Desventaja: punto único de fallo.
* **Distribuidos (DVCS):** Cada desarrollador tiene copia completa (Git, Mercurial). Ventaja: flexibilidad, offline.

### 6.3. Herramientas

* **Git:** El DVCS más popular.
* **Subversion (SVN):** CVCS maduro.
* **Mercurial:** Otro DVCS.

### 6.4. Repositorio

* **Concepto:** Lugar donde el VCS almacena el historial.
* **Local:** Copia en máquina del desarrollador.
* **Remoto:** Copia en servidor (GitHub, GitLab) para colaboración/backup.

---

## 7. Elaboración de Diagramas de Clases (UML)

Diagrama de estructura estática UML: clases, atributos, operaciones y relaciones.

### 7.1. Notación de Clases

* Rectángulo: Nombre, Atributos, Operaciones.
* Visibilidad: `+` público, `-` privado, `#` protegido, `~` paquete.
* Atributos: `visibilidad nombre: tipo = valorPorDefecto`
* Métodos: `visibilidad nombre(parámetros): tipoDeRetorno`

### 7.2. Objetos e Instanciación

* **Objeto:** Instancia de clase (`nombreObjeto: NombreClase` subrayado).

### 7.3. Relaciones

* **Herencia:** Flecha hueca a superclase.
* **Composición:** Rombo relleno en el "todo" (parte no existe sin el todo).
* **Agregación:** Rombo hueco en el "todo" (parte puede existir independientemente).
* **Asociación:** Línea continua (puede tener multiplicidad).
* **Dependencia (Uso):** Línea discontinua con flecha.

### 7.4. Herramientas para Elaboración y Generación

StarUML, Visual Paradigm, Lucidchart, draw.io. IDEs con plugins. Permiten ingeniería directa (diagrama -> código) e inversa (código -> diagrama).

---

## 8. Elaboración de Diagramas de Comportamiento (UML)

Describen aspectos dinámicos del sistema.

### 8.1. Tipos Principales

* **Casos de Uso:** Funcionalidad desde perspectiva del usuario.
* **Interacción (Secuencia, Colaboración/Comunicación):** Colaboración entre objetos.
* **Estados (Máquina de Estados):** Ciclo de vida de un objeto.
* **Actividad:** Flujo de trabajo o procesos.

### 8.2. Diagramas de Casos de Uso

* **Actor:** Rol (figura de palo).
* **Caso de Uso:** Funcionalidad (óvalo).
* **Relación de Comunicación:** Línea actor-caso de uso.

### 8.3. Diagramas de Interacción

* **Diagramas de Secuencia:** Orden temporal de mensajes.
    * **Línea de Vida:** Vertical discontinua.
    * **Activación:** Rectángulo en línea de vida.
    * **Mensaje:** Flecha entre líneas de vida.
* **Diagramas de Colaboración/Comunicación:** Organización estructural de objetos.
    * **Objetos:** Rectángulos.
    * **Enlaces:** Líneas.
    * **Mensajes:** Flechas numeradas en enlaces.

### 8.4. Diagramas de Estados

* Modela estados y transiciones de un objeto.
* **Estado:** Rectángulo bordes redondeados.
* **Transición:** Flecha (causada por evento).
* **Evento:** Ocurrencia que dispara transición.
