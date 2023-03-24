# **POLIMORFISMO**


# **Introducción.**

El polimorfismo es uno de los conceptos más importantes de la programación orientada a objetos en Java. Este principio permite que un objeto pueda tener múltiples formas y ser tratado de diferentes maneras según el contexto en el que se use. En términos simples, el polimorfismo permite escribir código genérico que puede ser utilizado con diferentes tipos de objetos, lo que hace que el código sea más flexible y reutilizable.

  

En Java, el polimorfismo se logra a través de la herencia y la implementación de interfaces. Las subclases heredan los atributos y métodos de su clase base, pero también pueden agregar o sobrescribir estos elementos para adaptarse a sus propias necesidades. Además, las interfaces permiten que diferentes clases implementen un conjunto común de métodos, lo que hace que estas clases sean intercambiables en ciertos contextos.

  

El polimorfismo es una herramienta poderosa para escribir código eficiente y mantenible. Permite trabajar con objetos de diferentes clases como si fueran del mismo tipo, lo que simplifica el código y lo hace más fácil de entender y mantener. En este sentido, el polimorfismo es un principio fundamental de la programación orientada a objetos en Java, y es esencial para escribir software robusto y escalable.

## **Polimorfismo.**

El polimorfismo en Java es un concepto de programación orientada a objetos que permite que un objeto de una clase pueda ser tratado como si fuera un objeto de otra clase relacionada. Esto se logra a través de la herencia y la implementación de interfaces.

  

En términos simples, el polimorfismo en Java permite que una sola clase tenga múltiples formas. Por ejemplo, si hay una clase Animal que tiene un método llamado “hacerSonido()”, y luego se crean dos subclases: Perro y Gato. Cada subclase puede implementar su propia versión del método “hacerSonido()”, por lo que el método se comportará de manera diferente según el objeto que se esté utilizando en ese momento.

  

El polimorfismo en Java es útil porque permite escribir código más genérico y reutilizable, ya que se puede escribir código que trabaje con objetos de una clase base, y este codigo tambien funcionara con objetos de cualquier subclase que herede de esa clase base.

Además el polimorfismo puede hacer que el código sea más fácil de mantener, ya que se pueden agregar nuevas subclases sin tener que modificar el código existente.

## Un ejemplo sencillo de polimorfismo en Java.

En este apartado aplicaremos lo visto en la teoría. Implementaremos una clase **Vehículo** que tiene un método **mover()** que es sobreescrito por las clases **Coche** y **Bicicleta**.

Luego en el método **main**, se creará una instancia de la clase **Coche** y se asigna a una variable de tipo **Vehículo**. Eso es exactamente el polimorfismo.

Cuando se llama al método **mover()** en esa variable, se ejecuta el método de sobreescrito en la clase **Coche**. Lo mismo sucede cuando se asigna una instancia de la clase **Bicicleta** a la misma variable y se llama al método **mover()**.

## **Ejemplo Práctico.**

**Este código ilustra el concepto de polimorfismo en Java. Primero, hay una clase base llamada Vehiculo, que tiene un método llamado "mover" que simplemente imprime un mensaje que indica que el vehículo se está moviendo una cierta distancia.**

```
 class Vehiculo {
            public void mover(int distancia) {
                System.out.println("El vehículo se está moviendo " + distancia + " metros");
            }
        }
```




Luego, hay dos clases derivadas: Coche y Bicicleta. Ambas clases sobrescriben el método "mover" heredado de la clase Vehiculo, para proporcionar una implementación específica para el tipo de vehículo. El método "mover" en la clase Coche imprime un mensaje indicando que el coche está avanzando una cierta distancia y si lo hace rápido o lento, mientras que el método "mover" en la clase Bicicleta imprime un mensaje indicando que la bicicleta está pedaleando y si lo hace rápido o lento.

```
 class Coche extends Vehiculo {
            public void mover(int distancia) {
                System.out.println("El coche está avanzando " + distancia + " metros");
                if (distancia > 10) {
                    System.out.println("El coche está yendo rápido");
                } else {
                    System.out.println("El coche está yendo lento");
                }
            }
        }
        ```
   class Bicicleta extends Vehiculo {
            public void mover(int distancia) {
                System.out.println("La bicicleta está pedaleando " + distancia + " metros");
                if (distancia > 5) {
                    System.out.println("La bicicleta está yendo rápido");
                } else {
                    System.out.println("La bicicleta está yendo lento");
                }
            }
        }
```


En el método principal de la clase PolimorfismoEjemplo, se crea una instancia de Coche y se la asigna una variable de tipo Vehiculo llamada "miVehiculo". Luego, se llama al método "mover" en "miVehiculo", lo que resulta en que se ejecuta el método "mover" de la clase Coche, que imprime el mensaje correspondiente al movimiento del coche.

```
public class PolimorfismoEjemplo {
            public static void main(String[] args) {
                Vehiculo miVehiculo = new Coche();
                miVehiculo.mover(15); // El coche está avanzando 15 metros
                                     // El coche está yendo rápido
                miVehiculo = new Bicicleta();
                miVehiculo.mover(3); // La bicicleta está pedaleando 3 metros
                                     // La bicicleta está yendo lento
            }
        }
```

A continuación, se crea una instancia de Bicicleta y se la asigna a la misma variable "miVehiculo". Se llama al método "mover" en "miVehiculo" nuevamente, pero esta vez se ejecuta el método "mover" de la clase Bicicleta, que imprime el mensaje correspondiente al movimiento de la bicicleta.

Este ejemplo muestra cómo un objeto de una clase derivada puede ser tratado como un objeto de la clase base, lo que permite escribir código genérico que puede ser utilizado con diferentes tipos de objetos. Esto hace que el código sea más flexible y reutilizable, y es una de las ventajas clave de la programación orientada a objetos en Java.





## **Conclusión.**

**Este ejemplo demuestra cómo el polimorfismo puede usarse para escribir código más genérico y reutilizable, permitiendo que diferentes objetos se comporten de manera diferente en el contexto en el que se utilice. Es una técnica fundamental en la programación orientada a objetos y es muy utilizada en aplicaciones Java.**