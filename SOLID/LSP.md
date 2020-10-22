# Liskov Sustitution Principle (OCP)

### Concepto
* Barbara Liskov habló primero de esto.
* Si S es un subtipo de T, instancias de T deberían poderse sustituir por instancias de S sin alterar las propiedades del programa
* Es decir, al tener una jerarquía nos supone que estamos estableciendo un contrato en el padre, por lo que, garantizar que se mantiene dicho contrato en el hijo, nos permitirá que podamos sustituir al padre y la aplicación seguirá funcionando perfectamente


### ¿Cómo?
* El comportamiento de de las subclases debe respetar el contrato establecido en la superclase.

### Finalidad
* Mantener correctitud funcional para poder aplicar OCP.

### Ejemplo

**Antes**

```java
class Rectangle {

    private Integer length;      
    private Integer width;

    Rectangle(Integer length, Integer width) {  
        this.length = length;
        this.width = width;
    }

    void setLength(Integer length) {
        this.length = length;
    }

    void setWidth(Integer width) {
        this.width = width;
    }

    Integer getArea() {
        return this.length * this.width;
    }
}
```

**Después**

```java
interface Measurable {
  public Double getTotalLength();
  public Double getSentLength();
}

final class Song implements Measurable {
    private Double totalLength;
    private Double sentLength;
    
    @Override
    public Double getTotalLength() {
        return totalLength;
    }
    
    @Override
    public Double getSentLength() {
        return sentLength;
    }
}

final class Progress {
    public Double getSentLengthPercentage(Measurable measurable) {
        return measurable.getSentLength() * 100 / measurable.getTotalLength();
    }
}
```

*Nuestra clase Progress realizará el cálculo en base a algo Measurable, por lo que se acopla únicamente a la interface*