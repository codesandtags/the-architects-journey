# Open Close Principle (OCP)

### Concepto
* El software debería estar abierto para la extensión y cerrado para la modificación


### ¿Cómo?
* No depender de implementaciones especificas

### Finalidad
* Facilidad de añadir nuevos casos de usos o funcionalidades

### Ejemplo

**Antes**

```java
final class Song {
  private Double totalLength;
  private Double sentLength;

  public Double getSentLengthPercentage() {
    return sentLength * 100 / totalLength;
  }
}

final class File {
  private Double totalLength;
  private Double sentLength;

  public Double getSentLengthPercentage() {
    return sentLength * 100 / totalLength;
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