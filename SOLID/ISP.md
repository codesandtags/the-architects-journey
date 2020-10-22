# Interface Segregation Principle (OCP)

### Concepto
* Ningún cliente debería verse forzado a depender de métodos que no usa.

### ¿Cómo?
* Definir contratos de interfaces basándonos en los clientes que las usan y no en las implementaciones que pudiéramos tener (Las interfaces pertenecen a los clientes)
* Evitar Header Interfaces promoviendo Role Interfaces.

### Finalidad
* Alta cohesión y bajo acoplamiento estructural.

### Ejemplo

**Antes**

```java
public interface Animal {
    void fly();
    void run();
    void bark();
}

public class Dog implements Animal {
    @Override
    public void fly() { }

    @Override
    public void run() {
        System.out.print("Dog is running");
    }

    @Override
    public void bark() {
        System.out.print("Dog is barking");
    }
}

public class Bird implements Animal {
    public void bark() { }
    public void run() {
        System.out.print("Bird is running");
    }
    public void fly() {
        System.out.print("Bird is flying");
    }
}
```

**Después**


```java
public interface Flyable {
    void fly();
}
public interface Runnable {
    void run();
}
public interface Barkable {
    void bark();
}

public class Dog implements Barkable, Runnable {
    @Override
    public void run() {
        System.out.print("Dog is running");
    }

    @Override
    public void bark() {
        System.out.print("Dog is barking");
    }
}

public class Bird implements Runnable, Flyable {
    @Override
    public void run() {
        System.out.print("Bird is running");
    }

    @Override
    public void fly() {
        System.out.print("Bird is flying");
    }
}
```


