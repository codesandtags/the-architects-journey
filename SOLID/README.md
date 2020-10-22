# Principios Solid

* Convenciones de diseño
* S = Single Responsibility Principle
* O = Open / Closed Principle
* L = Liskov Sustitution Principle
* I = Interface Segregation Principle
* D = Dependency Inversion Principle


"Las buenas practicas de hoy son los anti-patrones del mañana".
"Un gran poder conlleva una gran responsabilidad"

### STUPID vs SOLID

Estos son algunos anti patrones a tener en cuenta.

S = Singleton : Patrón de diseño ampliamente usado hace unos años. Evita exponer los colaboradores de una clase (algo negativo ya que hace más difícil de detectar el acoplamiento entre clases).

T = Tight Coupling : Acoplamiento entre clases que dificulta la mantenibilidad y tolerancia al cambio que proporciona la aplicación de principios SOLID.

U = Untestability : Código difícil de testear. Derivado de no inyectar dependencias vía constructor nos vemos obligados al uso de costuras en nuestro código.

P = Premature Optimization : Anticiparnos a los requisitos de nuestro software desarrollando abstracciones innecesarias que añaden complejidad.

I = Indescriptive Naming: Nomenclatura indescriptiva tanto a nivel de clases, como variables o atributos.

D = Duplication :  Duplicidad de código. Algo solucionable si aplicamos el Principio de Responsabilidad Única de SOLID e inyección de dependencias.



## Single Responsibility Principle (SRP)

### Concepto
* Una clase debe tener una única razón por la cual cambiar.
* Una clase = Un concepto y responsabilidad

### ¿Cómo?
* Clases de servicios con pequeños con objetivos acotados
* No dejar modelos de dominio muy genericos, para eso debemos utilizar nombres que acoten la responsabilidad.

### Finalidad
* Alto cohesión y robustez
* Permitir composición de clases
* Evitar duplicidad

### Ejemplo

```java
/**
 * ⚠️ Motivo del por qué no respetamos SRP: Book está acoplada 
 * al canal estándar de salida al imprimir la página actual. 
 * Sabe cómo modelar los datos y cómo imprimirlos.
 **/

final class Book
{
    public String getTitle()
    {
        return "A great book";
    }
    public String getAuthor()
    {
        return "John Doe";
    }
    public void printCurrentPage()
    { 
        System.out.println("current page content");
    }
}

final class Client
{
    public Client() {
        Book book = new Book(…);
        book.printCurrentPage();
    }
}
```

Después del refactor

```java
final class Book
{
    public String getTitle()
    {
        return "A great book";
    }
    public String getAuthor()
    {
        return "John Doe";
    }
    public String getCurrentPage()
    {
        return "current page content";
    }
}

interface Printer
{
    public void printPage(String page);
}

final class StandardOutputPrinter implements Printer
{
    public void printPage(String page)
    {
        System.out.println(page);
    }
}

final class StandardOutputHtmlPrinter implements Printer
{
    public void printPage(String page)
    {
        System.out.println("<div>" + page + "</div>");
    }
}
```

![Diagrama de clases de la solución con SRP](https://s3.amazonaws.com/pathwright-uploads/7y4pPpr7S2oKpSbjIgUx_Curso+SOLID.027.png)

## Open / Closed Principle
---

## Liskov Sustitution Principle
---

## Interface Segregation Principle
---

## Dependency Inversion Principle
---



### Resources
* https://pro.codely.tv/library/principios-solid-aplicados/
  