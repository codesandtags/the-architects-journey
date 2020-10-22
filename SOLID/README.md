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

**S = Singleton** : Patrón de diseño ampliamente usado hace unos años. Evita exponer los colaboradores de una clase (algo negativo ya que hace más difícil de detectar el acoplamiento entre clases).

**T = Tight Coupling:** Acoplamiento entre clases que dificulta la mantenibilidad y tolerancia al cambio que proporciona la aplicación de principios SOLID.

**U = Untestability:** Código difícil de testear. Derivado de no inyectar dependencias vía constructor nos vemos obligados al uso de costuras en nuestro código.

**P = Premature Optimization:** Anticiparnos a los requisitos de nuestro software desarrollando abstracciones innecesarias que añaden complejidad.

**I = Indescriptive Naming:** Nomenclatura indescriptiva tanto a nivel de clases, como variables o atributos.

**D = Duplication:**  Duplicidad de código. Algo solucionable si aplicamos el Principio de Responsabilidad Única de SOLID e inyección de dependencias.

* ### [Single Responsibility Principle (SRP)](SRP.md)
* ### [Open / Closed Principle (OCP)](OCP.md)
* ### [Liskov Sustitution Principle](LSP.md)
* ### [Interface Segregation Principle](ISP.md)
* ### [Dependency Inversion Principle](DIP.md)

### Resources
* https://pro.codely.tv/library/principios-solid-aplicados/
  