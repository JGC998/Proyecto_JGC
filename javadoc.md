# Documentación con Javadoc en Java

## 1. ¿Qué es Javadoc?
Javadoc es una herramienta del JDK (Java Development Kit) diseñada para generar documentación de API en formato HTML a partir de comentarios especiales en el código fuente Java. Su principal objetivo es facilitar la comprensión y el uso de las clases y métodos, especialmente en proyectos colaborativos o al desarrollar librerías para terceros.

**Ventajas:**
* **Documentación integrada con el código:** Facilita mantenerla sincronizada con los cambios.
* **Formato estándar y profesional:** Genera HTML navegable, ampliamente reconocido.
* **Soportado por IDEs:** Entornos como IntelliJ IDEA, Eclipse o NetBeans integran funcionalidades para Javadoc.

## 2. Sintaxis Básica de los Comentarios Javadoc
Cómo se escriben y dónde se colocan los comentarios Javadoc.

## 3. Etiquetas Javadoc (Block Tags)
Descripción de las principales etiquetas de bloque.

## 4. Etiquetas en Línea (Inline Tags)
Descripción de las principales etiquetas en línea.

## 5. Generación de la Documentación
Cómo generar el HTML con el comando `javadoc`.

## 6. Buenas Prácticas
Consejos para escribir buena documentación Javadoc.



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
