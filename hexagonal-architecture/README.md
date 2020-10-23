# Arquitectura Hexagonal | Ports & Adapters

## Beneficios
* Mantenibilidad
* Flexibilidad
* Simplicidad
* Mejor Testing

## ¿Qué es?
* Hace parte de las arquitecturas limpias

![Arquitecturas Limpias](https://xurxodev.com/content/images/2016/07/CleanArchitecture-8b00a9d7e2543fa9ca76b81b05066629.jpg)


**Infaestructura:** Código que cambia en función de decisiones externas. En esta capa vivirán las implementaciones de las interfaces que definiremos a nivel de dominio. Es decir, nos apoyaremos en el DIP de SOLID para poder desacoplarnos de las dependencias externas.

**Aplicación:** La capa de aplicación es donde viven los casos de uso de nuestra aplicación (registrar usuario, publicar producto, añadir producto al carrito, etc).

**Dominio:** Conceptos que están en nuestro contexto (Usuario, Producto, Carrito, etc), y reglas de negocio que vienen determinadas en exclusiva por nosotros (servicios de dominio),

![Ejemplo capas de la arquitectura hexagonal](https://s3.amazonaws.com/pathwright-uploads/ge22DKPbSOWYkS8Cj1eF_03%252BQue%2525CC%252581%252Bes%252Bla%252BArquitectura%252BHexagonal.key%252B2017-12-15%252B12-04-45.png)

![Ejemplo de flujo de datos en una arquitectura de puertos y adaptadores](https://s3.amazonaws.com/pathwright-uploads/09EkzTi5Sg2O1LmchmN0_03%252BQue%2525CC%252581%252Bes%252Bla%252BArquitectura%252BHexagonal.key%252B2017-12-15%252B12-10-33.png)

### Resources
* https://codurance.com/2015/05/12/does-tdd-lead-to-good-design/
* 
* https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)
* https://blog.octo.com/en/hexagonal-architecture-three-principles-and-an-implementation-example/