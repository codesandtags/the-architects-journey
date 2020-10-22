# Single Responsibility Principle (SRP)

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