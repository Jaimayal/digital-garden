---
title: "Shopify"
date: "2022-12-17 08:06"
tags: 
  - 
draft: true
---


## Elegir Temas
Se deben de tomar en cuenta cuatro criterios para elegir uno correctamente
1. Las sensaciones generales de usabilidad y diseño
2. Las funcionalidades que provee
3. Las funcionalidades que provee al desarrollador
4. Flexibilidad en las templates

De donde obtener temas?
- shopify themes
- outofthesandbox

### Buenos temas
#### free
- Debut. General, asesorias, bracaletas, jardineria. Tema mas mantenido
- Brooklyn. Para fashion y profesional
- Venture. Recreacional, tiendas generales, para pequeñas cosas
- Supply. Electronica, amazon like, muchos productos

#### premium
- Empire. Lo que sea que tenga que ver con comida, fresh delivery
- Prestige. Increible para fashion
- Impulse. Increible para fashion tambien
- Parallax. Increible. Recreacion fuera de casa, artes
- Turbo Theme. Increible para general, muy lleno de features
## Apps
Todas las aplicaciones de Shopify se pueden subidividir en dos grupos
- frontend. Tienen impacto en el performance
- backend. No tienen impacto 

Necesitamos hacer algo especial y no lo podemos ahcer sin una aplicacion
Lo que sea que necesite hacer una base de datos
Velocidad y costos de desarrollo


### Recomendadas
- BEST currency covnersion. Convercion de monedas. Shopify solo hace el display. En temas modernos se usa shopify payments
- Langify. Te permite traducir todo a otro idioma
- Metafields Guru. Te ayuda a manejar los metafields para guardar informacion
- Infinite Product Options. Te deja agregar mas de 99 variantes
- Excelify. Te ayuda a manejar muchas cosas de tu tienda con CSV files
- Smart Search / Instant Search. Integra la busqueda y hace que sea mas rapida
- Product Reviews -Judgme Reviews - Look Reviews. Te permite agregar opiniones a los productos
- Shogun / GemPages. Landpages, drag and drop
- Hotjar. Te permite generar heatmaps para saber que tanto se clickea un elemento, etc
- VWO. Te permite hacer A/B split tests para probar cosas diferentes
- Mailchimp. No tiene conexion a Shopify pero se puede utilizar ShopSync
- Klaviyo. Mucho mas profesional, te da automatizacion de emails.
- Order Printer PRO. Te permite imprimir en PDF las ordenes, hacer tracking y otros

## Page Speed Optimization
El problema no es con las optimizaciones, es con las expectativas de los clientes.
- Comparate con otras marcas gigantes

Lo que mas impacta el performance:
- Aplicaciones. Principalmente las activas en el frontend
- Imagenes. Siempre da un upload, no utilices un URL. Manten las imagenes de un buen ratio. Implementar lazy loading (Usar lazySizes)

## Migraciones
Moveres desde otro sistema hacia Shopify.

Cosas que necesitan migrarse
1. Datos
2. Contenido
3. Diseño
4. Codificacion / Necesidades Unicas
5. SEO

Nuestro servicio. 
- Store Setup
- Migracion de Datos
- Contenido e Imagenes
- Funcionalidades de la Tienda
- Training

Lo que no incluye
- Acceso a los datos
- Garantia de las Imagenes
- Costos por tema, aplicaciones, y otros.

### Como ejecutar una migracion
#### Datos
- Prudctos + reviews
- Clientes
- Historico de Ordenes

Special Inputs -> Metafields
Opciones para combinaciones -> Combinacion de Opciones o uso de una Aplicacion

Excelify para migrar.
Store Importer. Tambien sirve para migrar

#### Contenido
Excelify te permite importar blogs, y otras cosas.
- Necesitas descargar y resubir las imagenes
- Checar si contiene secciones especiales

#### Diseño
- Pixel perfect recreation es dificil
- Acercate lo maximo posible como facelift o lavado de cara
- Completa remake

#### Codificacion y necesidades especiales
Investiga las cosas que estan disponibles en la otra tienda y busca una solucion o alternativas para realizarlo.
- Multiples lenguajes?
- Multiples monedas?
- Ofertas o bundles?
- Suscripciones?
- Conectado a otros canales de ventas?
- Conectado a social media?
- Usan una red de fulfilment o un almacen?
- Esta conectado a tecnologias de marketing ?

#### SEO
Dominio y backlinks. 
Si se va a obtener un nuevo dominio por completo  se necesita implementar Domain Forwarding

Usar el mismo dominio. El problema es la estructura de URl, por lo que los links que vayan a  un elemento se van a romper. Para esto se necesita hacer URL redirect

1. Backend Setup + Backend Apps
2. Importar data y organizar productos
3. Importar contenido
4. Frontend Setup + Frontend Apps
5. Setear el dominio y los redirects


## Conversion Optimization
Busca optimizar al maximo la cantidad de reveneu generada a traves de la navegacion de los clientes en el.

### servicios
#### On Page
- Generar zonas de calor
- Split Testing
- Data Driven Optimizations

Mejorar el frontend de la tienda. El UX/UI. Todas estas mejoras tienen que estar dirigidas por DATOS. 

Las formas de hacerlo es hacer Split Testing y Generar Zonas de Calor
- Hotjar sirve para generar zonas de calor

La forma de probar cambios y sus impactos se deben usar A/B Split Test

- La tienda necesita 10,000 visitores por mes para poder validar los datos
- Concentrarte en cosas que tienen un mas alto impacto primero
- Optimizar para Revenue, no para nada mas

VWO sirve para hacer split testing. Es algo cara pero hace el trabajo bien.
Google Optimize. Es gratuita y tambien sirve para hacer split testing. Se necesita integrar Analytics para que funcione

Framework para A/B Testing
IF. \<lo que pasa\> THEN \<asumption\> BECAUSE \<justification\>.

#### Marketing
- Incrementar el valor de la orden promedio
- Market research

Incrementar el valor de la orden promedio. Incentivar a los clientes a comprar mas. Algunas cosas:
- Free Shipping
- In cart Upsells. (Ofertas en el carrito)
- Crear bundles de productos
- Discuentos Bulk (Al comprar vairos productos)
- Pagos por Suscripciones

Marketing Research. Crear un Buyer-Persona.

Descripcion detallada de la persona principal a la que va dirigido el ecommerce. Para esto puedes usar 
- Google Analytics. Entender al cliente
- Similarweb. Datos de sitios competidores
- Ubersuggest. Obtener las keywords que generan mayor entrada a la pagina

Recolecta la informacion en un documento profesional

#### Pricing
Debido a que debes trabajar con negocios ya establecidos. Por tanto:
- Development UI
- Order Boost
- Hotjar
- Heatmap Analysis. 
- AB Split Test. Por pagina o por mes
- Optimize. Gratis
- Buyer Persona. 


## Workflow
1. Solicita acceso a la tienda
2. Realiza una copia del tema actual
3. Trabaja en la copia, este servira como entorno de desarrollo.

## Theme Editing
Archivo importante theme.liquid. Tiene el contenido inicial de casi todos los archivos.

section 
Permite cargar todo el codigo que se encuentre dentro de una seccion del folder sections

contret for layout
Busca en la carpeta de  templates una que se adecue a la pagina que estamos visitando

include
Sirve para traer snippets que son piezas de codigo reutilizables.

- layout. Contenido que se encuentra en multiples paginas
- sections. Secciones de codigo reutilizables por el layout
- templates. Contenido que es renderizado pagina por pagina
- snippets. Piezas de codigo reutilizables en multiples paginas
- assets. se encuentra el codigo CSS y JS
- config. Se guardan las configuraciones del tema
- locales. se encuentra toda la informacion de texto plano incluidas multiples traducciones