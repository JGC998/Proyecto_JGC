# Documentación con Javadoc en Java

## 1. ¿Qué es Javadoc?
Javadoc es una herramienta del JDK (Java Development Kit) diseñada para generar documentación de API en formato HTML a partir de comentarios especiales en el código fuente Java. Su principal objetivo es facilitar la comprensión y el uso de las clases y métodos, especialmente en proyectos colaborativos o al desarrollar librerías para terceros.

**Ventajas:**
* **Documentación integrada con el código:** Facilita mantenerla sincronizada con los cambios.
* **Formato estándar y profesional:** Genera HTML navegable, ampliamente reconocido.
* **Soportado por IDEs:** Entornos como IntelliJ IDEA, Eclipse o NetBeans integran funcionalidades para Javadoc.

## 2. Sintaxis Básica de los Comentarios Javadoc

Los comentarios Javadoc son la base para generar documentación externa de la API de tu código Java. Tienen una sintaxis específica que los distingue de los comentarios regulares (`// ...` o `/* ... */`). El propósito fundamental es permitir que la herramienta `javadoc` (parte del JDK) analice estos comentarios y genere una documentación HTML bien estructurada y fácil de navegar.

**Cómo se escriben:**
* Un comentario Javadoc comienza con una barra inclinada seguida de dos asteriscos: `/**`. Este es el delimitador de inicio que la herramienta `javadoc` reconoce.
* Termina con un asterisco seguido de una barra inclinada: `*/`. Este es el delimitador de fin.
* Todo el texto contenido entre estos delimitadores `/** ... */` se considera parte del comentario Javadoc.
* Por convención, y para mejorar la legibilidad tanto en el código fuente como en el HTML generado (si se usan etiquetas como `<pre>`), cada línea subsiguiente dentro del bloque de comentario Javadoc suele comenzar con un asterisco (`*`) alineado verticalmente con los asteriscos del delimitador de apertura. Este asterisco inicial en cada línea es ignorado por la herramienta `javadoc` al procesar el contenido.

    ```java
    /**
     * Este es un comentario Javadoc simple.
     * Describe la funcionalidad de una clase o método.
     * Puede incluir múltiples líneas para mayor claridad y detalle.
     * La herramienta Javadoc ignorará el espacio en blanco inicial y el '*'
     * al principio de estas líneas.
     */
    ```

**Dónde se colocan:**
La regla fundamental es que un comentario Javadoc debe preceder **inmediatamente** a la declaración del elemento de código que está documentando. No debe haber ninguna otra sentencia de Java (como imports o anotaciones no destinadas a Javadoc) ni comentarios normales entre el final del comentario Javadoc (`*/`) y la declaración del elemento (clase, interfaz, método, constructor o campo).

Los comentarios Javadoc se pueden aplicar a los siguientes elementos del programa:

1.  **Declaraciones de Clase:**
    Se coloca justo antes de la palabra clave `class` (o `enum`, `record`). Describe el propósito general de la clase, sus responsabilidades principales, su rol en la arquitectura del sistema, y cualquier información relevante sobre su uso o invariantes.
    ```java
    /**
     * La clase {@code Usuario} modela un usuario en el sistema de gestión de la biblioteca.
     * Almacena información personal como nombre, ID de miembro, y también
     * gestiona el historial de préstamos y devoluciones.
     * Esta clase es fundamental para las operaciones de préstamo y autenticación.
     */
    public class Usuario {
        // ... cuerpo de la clase ...
    }
    ```

2.  **Declaraciones de Interfaz:**
    Similar a las clases, se coloca antes de la palabra clave `interface`. Describe el contrato que la interfaz define, el propósito de cada método que las clases implementadoras deberán proporcionar, y el tipo de comportamiento esperado.
    ```java
    /**
     * La interfaz {@code Imprimible} define el contrato para objetos
     * que pueden generar una representación en cadena de sí mismos para ser
     * mostrada en una impresora o consola.
     */
    public interface Imprimible {
        /**
         * Genera la representación en cadena para la impresión.
         * @return una cadena formateada lista para imprimir.
         */
        String obtenerTextoParaImpresion();
    }
    ```

3.  **Declaraciones de Métodos (incluyendo Constructores):**
    Se coloca antes de la firma del método o constructor. Debe describir qué hace el método (su acción o el valor que calcula), el propósito y restricciones de cada parámetro, qué devuelve (si aplica, incluyendo el significado de valores especiales como `null` o colecciones vacías), y qué excepciones puede lanzar y bajo qué condiciones.
    ```java
    /**
     * Calcula el total de una factura sumando los importes de sus líneas,
     * aplicando los impuestos correspondientes a cada línea.
     *
     * @param lineasFactura una lista de objetos {@code LineaFactura}, no debe ser nula y
     * no debe contener elementos nulos. Cada línea debe tener un precio válido.
     * @param tasaImpuesto la tasa de impuesto a aplicar como un decimal (ej. 0.21 para 21%).
     * Debe ser un valor no negativo.
     * @return el importe total de la factura incluyendo impuestos, como un {@code double}.
     * Devuelve 0.0 si la lista de líneas está vacía.
     * @throws IllegalArgumentException si la lista de {@code lineasFactura} es nula o si
     * {@code tasaImpuesto} es negativa.
     */
    public double calcularTotalFacturaConImpuestos(List<LineaFactura> lineasFactura, double tasaImpuesto) {
        // ... implementación ...
    }

    /**
     * Constructor para crear un objeto {@code Producto} con todos sus detalles.
     *
     * @param id el identificador único del producto, no puede ser nulo ni vacío.
     * @param nombre el nombre descriptivo del producto, no puede ser nulo ni vacío.
     * @param precio el precio unitario del producto, debe ser mayor o igual a cero.
     * @throws IllegalArgumentException si alguno de los parámetros no cumple las restricciones.
     */
    public Producto(String id, String nombre, double precio) {
        // ... implementación ...
    }
    ```

4.  **Declaraciones de Campos (Variables de instancia y de clase):**
    Se coloca antes de la declaración del campo. Describe el propósito del campo, su tipo, cualquier restricción sobre sus valores (ej. rango, si puede ser nulo), su valor inicial si es relevante, o si es una constante.
    ```java
    /**
     * Almacena el nombre completo del cliente.
     * Este campo es obligatorio y no puede ser nulo después de la inicialización
     * a través del constructor o un método setter apropiado.
     * Se espera que el formato sea "Apellidos, Nombre".
     */
    private String nombreCliente;

    /**
     * Constante que define la tasa de IVA aplicable por defecto (ej. 21%).
     * El valor se expresa como un decimal (ej. 0.21 para 21%).
     * Su valor actual es {@value}. Este valor puede ser configurado
     * a través de un archivo de propiedades externo en futuras versiones.
     */
    public static final double TASA_IVA_POR_DEFECTO = 0.21;
    ```

**La Frase Resumen (Summary Sentence):**
La **primera frase** de cualquier comentario Javadoc es crucial. Se considera la "frase resumen" y debe ser una descripción concisa y autoexplicativa del elemento documentado. La herramienta `javadoc` extrae esta primera frase para mostrarla en los índices y tablas resumen de la documentación generada (por ejemplo, en la lista de métodos de una clase).
Una frase resumen termina con el primer carácter de puntuación de fin de frase (`.`) seguido por un espacio, tabulador o un carácter de fin de línea. El texto que sigue después de esta frase resumen se considera parte de la descripción general más detallada.

```java
/**
 * Valida las credenciales del usuario contra la base de datos. Esta es la frase resumen.
 * <p>
 * Este método primero verifica que el nombre de usuario y la contraseña no sean nulos o vacíos.
 * Luego, consulta el repositorio de usuarios para encontrar un usuario coincidente.
 * Si las credenciales son correctas, se actualiza la fecha del último acceso del usuario.
 * En caso contrario, se registra el intento fallido para fines de auditoría y seguridad.
 * </p>
 * * <ul>
 * <li>La comparación de contraseñas es sensible a mayúsculas y minúsculas.</li>
 * <li>Se recomienda el uso de contraseñas seguras.</li>
 * </ul>
 *
 * @param nombreUsuario el nombre de usuario a validar. No debe ser {@code null}.
 * @param contrasena la contraseña proporcionada por el usuario. No debe ser {@code null}.
 * @return {@code true} si la autenticación es exitosa y el usuario está activo, {@code false} en caso contrario.
 */
public boolean autenticarUsuario(String nombreUsuario, String contrasena) {
    // ...
}



## Ejemplo Práctico: Clase `PuntoGeometrico`
Para ilustrar los conceptos de Javadoc, utilizaremos una clase sencilla `PuntoGeometrico` que representa un punto en un plano 2D.

```java
package com.ejemplo.geometria;

/**
 * Representa un punto en un plano cartesiano bidimensional (x, y).
 * <p>
 * Esta clase proporciona funcionalidades para obtener y modificar las coordenadas,
 * calcular la distancia a otro punto y representarse como una cadena de texto.
 * </p>
 *
 * @author jgc
 * @version 1.0
 * @since 1.0
 */
public class PuntoGeometrico {

    /**
     * Coordenada X del punto. Es un valor de tipo {@code double}.
     */
    private double x;

    /**
     * Coordenada Y del punto. Es un valor de tipo {@code double}.
     */
    private double y;

    /**
     * Constructor para crear un {@code PuntoGeometrico} con coordenadas específicas.
     *
     * @param x La coordenada X inicial del punto.
     * @param y La coordenada Y inicial del punto.
     */
    public PuntoGeometrico(double x, double y) {
        this.x = x;
        this.y = y;
    }

    /**
     * Obtiene la coordenada X de este punto.
     *
     * @return La coordenada X actual.
     */
    public double getX() {
        return x;
    }

    /**
     * Obtiene la coordenada Y de este punto.
     *
     * @return La coordenada Y actual.
     */
    public double getY() {
        return y;
    }

    /**
     * Establece una nueva coordenada X para este punto.
     *
     * @param nuevaX La nueva coordenada X que se asignará al punto.
     */
    public void setX(double nuevaX) {
        this.x = nuevaX;
    }

    /**
     * Establece una nueva coordenada Y para este punto.
     *
     * @param nuevaY La nueva coordenada Y que se asignará al punto.
     */
    public void setY(double nuevaY) {
        this.y = nuevaY;
    }

    /**
     * Calcula la distancia euclidiana entre este punto y otro punto proporcionado.
     * La fórmula utilizada es: sqrt((x2-x1)^2 + (y2-y1)^2).
     *
     * @param otroPunto El otro {@code PuntoGeometrico} al cual se calculará la distancia.
     * No debe ser {@code null}.
     * @return La distancia calculada entre los dos puntos.
     * @throws IllegalArgumentException si {@code otroPunto} es {@code null}.
     * @see <a href="[https://es.wikipedia.org/wiki/Distancia_euclidiana](https://es.wikipedia.org/wiki/Distancia_euclidiana)">Distancia Euclidiana</a>
     */
    public double calcularDistancia(PuntoGeometrico otroPunto) {
        if (otroPunto == null) {
            throw new IllegalArgumentException("El otro punto no puede ser nulo.");
        }
        double diffX = otroPunto.x - this.x;
        double diffY = otroPunto.y - this.y;
        return Math.sqrt(diffX * diffX + diffY * diffY);
    }

    /**
     * Devuelve una representación en cadena de este punto.
     * El formato es "(x, y)". Por ejemplo, "(3.0, 4.5)".
     * <p>
     * Este método sobreescribe el método {@code toString} de la clase {@link Object}.
     * </p>
     *
     * @return Una cadena que representa las coordenadas del punto.
     */
    @Override
    public String toString() {
        return "(" + x + ", " + y + ")";
    }

    /**
     * Método de ejemplo para demostrar la etiqueta {@literal @deprecated}.
     *
     * @deprecated Desde la versión 1.1, este método es obsoleto.
     * Utilice {@link #calcularDistancia(PuntoGeometrico)} en su lugar,
     * ya que ofrece mayor claridad.
     * @param x2 Coordenada X del segundo punto.
     * @param y2 Coordenada Y del segundo punto.
     * @return La distancia al punto (x2, y2).
     */
    @Deprecated
    public double distanciaA(double x2, double y2) {
        PuntoGeometrico temp = new PuntoGeometrico(x2, y2);
        return calcularDistancia(temp);
    }
}
