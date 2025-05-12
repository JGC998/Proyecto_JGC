# Optimización del Código y Refactorización

## 1. Refactorización: Concepto y Limitaciones

### 1.1. ¿Qué es la Refactorización?

La **refactorización** (del inglés *refactoring*) es el proceso de reestructurar código existente —cambiando su estructura interna— sin modificar su comportamiento externo. El objetivo principal es mejorar atributos no funcionales del software, como la legibilidad, la mantenibilidad, la eficiencia (aunque no siempre es el foco principal de la refactorización clásica), y reducir la complejidad del código.

En esencia, refactorizar es "limpiar" el código para que sea más fácil de entender, de modificar y de extender en el futuro. No se trata de añadir nueva funcionalidad ni de corregir errores (aunque a veces, al refactorizar, se pueden descubrir bugs latentes).

**Características clave de la refactorización:**
* **No altera el comportamiento observable:** Un programa refactorizado debe pasar las mismas pruebas que antes de la refactorización.
* **Se aplica en pequeños pasos:** Cada cambio es pequeño y verificable.
* **Mejora la estructura interna:** Hace el código más comprensible, flexible y menos propenso a errores.
* **Se apoya en pruebas automatizadas:** Las pruebas garantizan que no se introduzcan regresiones.

### 1.2. Objetivos de la Refactorización

Los principales motivos para refactorizar incluyen:

* **Mejorar la legibilidad:** Un código más claro es más fácil de entender por otros desarrolladores (o por uno mismo en el futuro).
* **Reducir la complejidad:** Simplificar estructuras complejas facilita el razonamiento sobre el código.
* **Facilitar la mantenibilidad:** Un código bien estructurado es más fácil de modificar, corregir y extender sin introducir nuevos problemas.
* **Hacer el código más robusto:** Al eliminar duplicación y mejorar la cohesión, se reduce la probabilidad de errores.
* **Preparar el código para nuevas funcionalidades:** A veces es necesario refactorizar antes de poder añadir una nueva característica de forma limpia.
* **Encontrar bugs:** Aunque no es su objetivo principal, el proceso de entender y reestructurar código a menudo revela errores ocultos.

### 1.3. Limitaciones de la Refactorización

A pesar de sus beneficios, la refactorización tiene ciertas limitaciones y consideraciones:

* **No es una "bala de plata":** No soluciona problemas de diseño arquitectónico profundos por sí sola, aunque puede ser un primer paso.
* **Requiere tiempo y esfuerzo:** Aunque se haga en pequeños pasos, la refactorización consume tiempo que podría dedicarse a desarrollar nuevas funcionalidades. Es una inversión a largo plazo.
* **Riesgo de introducir errores (si no hay pruebas):** Si no se cuenta con un buen conjunto de pruebas automatizadas, es fácil romper algo sin darse cuenta. *Las pruebas son cruciales.*
* **No siempre mejora el rendimiento:** Algunas refactorizaciones pueden incluso degradar ligeramente el rendimiento en favor de la claridad. La optimización del rendimiento es un objetivo diferente, aunque a veces puede ir de la mano con un código más limpio.
* **Difícil de justificar en algunos entornos:** Puede ser complicado explicar a la gerencia no técnica la necesidad de invertir tiempo en "limpiar código" que "ya funciona".
* **No reemplaza la necesidad de un buen diseño inicial:** Es mejor diseñar bien desde el principio, aunque la refactorización es una herramienta valiosa para cuando el diseño inevitablemente necesita evolucionar o mejorar.
* **"Parálisis por refactorización":** Existe el riesgo de caer en un ciclo de refactorización continua sin entregar valor tangible si no se tiene un objetivo claro.


### 1.4. Patrones de Refactorización Más Usuales

Los patrones de refactorización son soluciones probadas a problemas comunes de diseño o "malos olores" (code smells) en el código. Ayudan a aplicar cambios de forma sistemática y segura. A continuación, se describen algunos de los más comunes, con ejemplos conceptuales en Java.

**a) Extraer Método (Extract Method)**

* **Problema:** Tienes un fragmento de código dentro de un método más largo que se puede agrupar lógicamente.
* **Solución:** Mover ese fragmento a un nuevo método con un nombre descriptivo y llamar al nuevo método desde el original.
* **Beneficios:** Mejora la legibilidad, reduce la duplicación si el fragmento se usa en varios sitios, y permite un mayor nivel de abstracción.

    *Antes:*
    ```java
    void imprimirResumenPedido(Pedido pedido) {
        double total = 0;
        // Calcular total
        for (Item item : pedido.getItems()) {
            total += item.getPrecio() * item.getCantidad();
        }

        // Imprimir detalles del cliente
        System.out.println("Cliente: " + pedido.getCliente().getNombre());
        System.out.println("Dirección: " + pedido.getCliente().getDireccion());

        // Imprimir total
        System.out.println("Total del pedido: " + total);
    }
    ```

    *Después:*
    ```java
    void imprimirResumenPedido(Pedido pedido) {
        double total = calcularTotal(pedido);
        imprimirDetallesCliente(pedido.getCliente());
        System.out.println("Total del pedido: " + total);
    }

    private double calcularTotal(Pedido pedido) {
        double total = 0;
        for (Item item : pedido.getItems()) {
            total += item.getPrecio() * item.getCantidad();
        }
        return total;
    }

    private void imprimirDetallesCliente(Cliente cliente) {
        System.out.println("Cliente: " + cliente.getNombre());
        System.out.println("Dirección: " + cliente.getDireccion());
    }
    ```

**b) Renombrar Variable / Método / Clase (Rename Variable / Method / Class)**

* **Problema:** El nombre de una variable, método o clase no revela claramente su propósito.
* **Solución:** Cambiar el nombre por uno más descriptivo.
* **Beneficios:** Mejora drásticamente la comprensión del código.

    *Antes:*
    ```java
    double val; // ¿Qué valor?
    void proc(List<String> d) { /* ... */ } // ¿Qué procesa? ¿Qué es d?
    ```

    *Después:*
    ```java
    double impuestoCalculado;
    void procesarLineasDeFactura(List<String> lineasFactura) { /* ... */ }
    ```

**c) Encapsular Campo (Encapsulate Field)**

* **Problema:** Un campo público es accedido directamente desde fuera de la clase.
* **Solución:** Hacer el campo privado y proporcionar métodos públicos (getters/setters) para acceder y modificar su valor.
* **Beneficios:** Mejora el control sobre el acceso al campo, permite añadir lógica (validación, logging) en los getters/setters, y facilita cambios futuros en la representación interna del campo sin afectar a los clientes de la clase.

    *Antes:*
    ```java
    public class Jugador {
        public String nombre; // Acceso directo
        public int puntuacion;
    }
    // En otra clase:
    // jugador.puntuacion = 100;
    ```

    *Después:*
    ```java
    public class Jugador {
        private String nombre;
        private int puntuacion;

        public String getNombre() {
            return nombre;
        }
        public void setNombre(String nombre) {
            this.nombre = nombre;
        }
        public int getPuntuacion() {
            return puntuacion;
        }
        public void setPuntuacion(int puntuacion) {
            if (puntuacion >= 0) { // Se puede añadir lógica de validación
                this.puntuacion = puntuacion;
            }
        }
    }
    // En otra clase:
    // jugador.setPuntuacion(100);
    ```

**d) Reemplazar Número Mágico con Constante Simbólica (Replace Magic Number with Symbolic Constant)**

* **Problema:** Se usa un número literal (un "número mágico") en el código sin una explicación clara de su significado.
* **Solución:** Definir una constante con un nombre descriptivo y usarla en lugar del número.
* **Beneficios:** Mejora la legibilidad y la mantenibilidad (si el valor necesita cambiar, solo se modifica en un lugar).

    *Antes:*
    ```java
    if (estado == 3) { // ¿Qué significa 3?
        // ...
    }
    double totalConImpuesto = precioBase * 1.21; // ¿Qué es 1.21?
    ```

    *Después:*
    ```java
    public static final int ESTADO_PROCESADO = 3;
    public static final double TASA_IVA_GENERAL = 0.21;
    // ...
    if (estado == ESTADO_PROCESADO) {
        // ...
    }
    double totalConImpuesto = precioBase * (1 + TASA_IVA_GENERAL);
    ```

**e) Introducir Variable Explicativa (Introduce Explaining Variable)**

* **Problema:** Una expresión compleja es difícil de entender.
* **Solución:** Dividir la expresión en partes más pequeñas, asignando cada parte a una variable con un nombre descriptivo.
* **Beneficios:** Mejora la legibilidad y facilita la depuración.

    *Antes:*
    ```java
    if ((plataforma.toUpperCase().indexOf("MAC") > -1) &&
        (navegador.toUpperCase().indexOf("IE") > -1) &&
         fueRedimensionado() && (version > 5)) {
        // hacer algo
    }
    ```

    *Después:*
    ```java
    final boolean esMac = plataforma.toUpperCase().indexOf("MAC") > -1;
    final boolean esInternetExplorer = navegador.toUpperCase().indexOf("IE") > -1;
    final boolean esVersionAntiguaIE = version > 5; // Asumiendo que 5 es una versión antigua

    if (esMac && esInternetExplorer && fueRedimensionado() && esVersionAntiguaIE) {
        // hacer algo
    }
    ```
**f) Mover Método (Move Method)**

* **Problema:** Un método está en una clase pero interactúa más con otra clase (usa más características de la otra clase que de la suya propia).
* **Solución:** Mover el método a la clase con la que tiene mayor afinidad.
* **Beneficios:** Mejora la cohesión de las clases y reduce el acoplamiento.

    *(Ejemplo conceptual)*
    *Antes:* `ClaseA` tiene un método `metodoQueUsaMuchoDeClaseB(ClaseB objB)`
    *Después:* `ClaseB` ahora tiene `metodoMovido()` y `ClaseA` llama a `objB.metodoMovido()`.

**g) Extraer Clase (Extract Class)**

* **Problema:** Una clase tiene demasiadas responsabilidades o representa dos o más conceptos diferentes.
* **Solución:** Crear una nueva clase y mover los campos y métodos relacionados con una de las responsabilidades a esta nueva clase.
* **Beneficios:** Mejora la cohesión, sigue el Principio de Responsabilidad Única (SRP).

    *(Ejemplo conceptual)*
    *Antes:* `ClasePersona` maneja datos personales y también datos de dirección.
    *Después:* `ClasePersona` y `ClaseDireccion`, donde `ClasePersona` tiene una instancia de `ClaseDireccion`.

*(Nota: Hay muchos más patrones de refactorización. Estos son solo algunos de los más fundamentales. Herramientas como los IDEs modernos suelen ofrecer soporte automatizado para muchos de ellos.)*

### 1.5. Refactorización y Pruebas: Una Relación Indispensable

La refactorización y las pruebas automatizadas están intrínsecamente ligadas. De hecho, **intentar refactorizar código sin un conjunto robusto de pruebas automatizadas es arriesgado y propenso a introducir errores (regresiones)**.

**¿Por qué son cruciales las pruebas al refactorizar?**

1.  **Red de Seguridad:**
    * Las pruebas actúan como una red de seguridad. El principio fundamental de la refactorización es cambiar la estructura interna del código *sin alterar su comportamiento externo observable*. Las pruebas automatizadas son la forma más eficaz de verificar que este principio se cumple.
    * Si después de una refactorización todas las pruebas siguen pasando, se tiene una alta confianza de que no se ha roto nada. Si alguna prueba falla, indica que el cambio introdujo un error.

2.  **Confianza para Realizar Cambios:**
    * Saber que se cuenta con una buena cobertura de pruebas da a los desarrolladores la confianza necesaria para realizar cambios estructurales, incluso en código complejo o delicado. Sin pruebas, el miedo a romper algo puede llevar a la inacción y al deterioro progresivo del código.

3.  **Detección Temprana de Errores:**
    * Si una refactorización introduce un bug, las pruebas lo detectarán inmediatamente (o la próxima vez que se ejecuten). Esto permite corregir el error de forma rápida y sencilla, cuando el cambio aún está fresco en la mente del desarrollador. Encontrar un bug introducido por una refactorización días o semanas después es mucho más costoso.

4.  **Facilitan Refactorizaciones Agresivas:**
    * Con una buena suite de pruebas, se pueden acometer refactorizaciones más ambiciosas y profundas con menor riesgo.

5.  **Documentación Viva del Comportamiento:**
    * Las pruebas también sirven como una forma de documentación ejecutable que describe cómo se espera que funcione el código. Al refactorizar, estas pruebas ayudan a asegurar que la nueva estructura sigue cumpliendo con esos comportamientos esperados.

**El Ciclo Refactorización-Pruebas:**

Un flujo de trabajo común es:

1.  **Asegurarse de tener pruebas:** Antes de refactorizar, verificar que existen pruebas para la sección de código que se va a modificar y que todas están pasando. Si no hay pruebas suficientes, escribirlas *antes* de refactorizar.
2.  **Refactorizar en pequeños pasos:** Aplicar un cambio pequeño y específico (ej. aplicar un patrón de refactorización).
3.  **Ejecutar las pruebas:** Después de cada pequeño cambio, ejecutar todas las pruebas relevantes.
    * Si todas pasan: Continuar con el siguiente pequeño paso de refactorización o dar por concluida la tarea.
    * Si alguna falla: Deshacer el último cambio (si es trivial) o depurar y corregir el error inmediatamente. Las pruebas ayudan a aislar el problema al último cambio realizado.
4.  **Repetir:** Continuar este ciclo hasta que el código alcance el estado deseado.

**¿Qué pasa si no hay pruebas?**

Si te enfrentas a código que necesita refactorización pero carece de pruebas (código heredado o *legacy code*), el primer paso antes de una refactorización significativa debería ser **escribir pruebas de caracterización**. Estas pruebas no juzgan si el código es correcto, sino que capturan su comportamiento actual, con sus virtudes y defectos. Una vez que se tiene esta red de seguridad, se puede empezar a refactorizar con más confianza.

En resumen, las pruebas no son solo una buena práctica en el desarrollo de software en general, sino un **requisito previo indispensable para una refactorización segura y efectiva.**

### 1.6. Herramientas de Ayuda a la Refactorización

Aunque la refactorización puede realizarse manualmente, los Entornos de Desarrollo Integrado (IDEs) modernos proporcionan un potente conjunto de herramientas que automatizan muchos patrones de refactorización comunes. Estas herramientas son extremadamente útiles porque:

* **Reducen el riesgo de error humano:** Realizan los cambios de forma sistemática y se encargan de actualizar todas las referencias necesarias (por ejemplo, al renombrar un método).
* **Ahorran tiempo:** Automatizan tareas que manualmente serían tediosas y propensas a errores.
* **Facilitan el aprendizaje:** Al ver cómo el IDE aplica una refactorización, los desarrolladores pueden aprender mejor los patrones y cuándo aplicarlos.

**Funcionalidades Comunes en los IDEs (ej. IntelliJ IDEA, Eclipse, VS Code con extensiones Java):**

La mayoría de los IDEs ofrecen menús contextuales (generalmente al hacer clic derecho sobre un elemento del código o a través de atajos de teclado) con opciones de refactorización como:

* **Renombrar (Rename):** Para variables, métodos, clases, paquetes, etc. El IDE actualiza todas las apariciones.
* **Extraer Método (Extract Method):** Seleccionas un bloque de código y el IDE lo convierte en un nuevo método, preguntando por su nombre y parámetros.
* **Extraer Variable (Extract Variable):** Para asignar una expresión a una nueva variable.
* **Extraer Constante (Extract Constant):** Similar a extraer variable, pero para crear una constante `public static final`.
* **Extraer Parámetro (Extract Parameter):** Si un método usa un valor que podría ser un parámetro, esta opción lo convierte en uno.
* **Extraer Interfaz (Extract Interface):** Crea una interfaz a partir de los métodos públicos de una clase.
* **Extraer Superclase (Extract Superclass):** Mueve miembros comunes de una o varias clases a una nueva superclase.
* **Mover (Move):** Permite mover clases entre paquetes, o métodos y campos estáticos entre clases.
* **Encapsular Campos (Encapsulate Fields):** Convierte campos públicos en privados y genera getters/setters.
* **Cambiar Firma de Método (Change Method Signature):** Permite añadir, eliminar o reordenar parámetros, cambiar el tipo de retorno o la visibilidad. El IDE intenta actualizar todos los sitios donde se llama al método.
* **Inline (Variable, Method):** Es la operación inversa a "Extraer". Reemplaza el uso de una variable o método con su contenido directamente en el sitio de la llamada. Útil si la abstracción ya no es necesaria o añade confusión.
* **Reemplazar Número Mágico con Constante (Replace Magic Number with Constant):** Detecta literales numéricos y ayuda a convertirlos en constantes.

**Uso Efectivo de las Herramientas:**

* **Conoce los atajos de teclado:** Agiliza mucho el proceso.
* **Previsualiza los cambios:** Muchos IDEs ofrecen una vista previa de los cambios antes de aplicarlos. Revísala.
* **Trabaja en conjunto con tu sistema de control de versiones (Git):** Haz commit de los cambios después de una refactorización exitosa (y verificada por pruebas) para poder revertir si algo sale mal.
* **No confíes ciegamente:** Aunque las herramientas son potentes, siempre es bueno entender qué está haciendo la refactorización y revisar el resultado, especialmente en casos complejos.

El uso de estas herramientas integradas en los IDEs es una práctica estándar y altamente recomendada para realizar refactorizaciones de manera eficiente y segura.
