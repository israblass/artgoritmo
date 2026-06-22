---
tipo: spec
producto: Artgoritmo Landing Corporativa
slug: artgoritmo-landing
actor: visitante-corporativo
pipeline: spec-builder
alimenta-a: plan-builder
tags: [spec, artgoritmo-landing, visitante-corporativo, plan-pendiente]
relacionados:
  - "[[plan artgoritmo-landing]]"
---

# Especificacion: Artgoritmo Landing Corporativa

## 1. Historia de Usuario

Un amigo me pidio montar una landing para Artgoritmo (Grupo Artgoritmo, J-50209850-0), una empresa venezolana con dos lineas de negocio: impresos publicitarios (roll ups, backings, banderines, stands, aranas, chupetas, tazas, gorras, impresion en vinil/banner/clean) y desarrollo de sistemas/software (sistemas para aseguradoras como La Venezolana de Seguros y Vida, y UbikGo/Uvic para polizas de grua). La landing debe captar clientes corporativos, con enfasis fuerte en la parte de sistemas porque los clientes target son del rubro de desarrollo de sistemas y quieren que lo que se les muestre les guste para cotizar con Artgoritmo. Tambien debe mostrar la parte de impresos pero con menor peso. Los textos de vision y concepto ya existen. La estetica es dark/tech (fondo negro con textura de poligonos, tipografia geometrica gris claro, acentos plateados). Se tiene un DESIGN.md basado en Linear como referencia de estilo. El destino de deploy es Vercel o un link HTML estatico.

## 2. Objetivo

Crear una landing page corporativa single-page para Grupo Artgoritmo que posicione a la empresa como proveedor de desarrollo de sistemas a medida y produccion de impresos publicitarios ante decisores corporativos (gerentes de IT, directores de operaciones, CEOs de aseguradoras y empresas medianas en Venezuela), generando contacto via WhatsApp o formulario.

## 3. Alcance

**Incluye:**
- Landing page single-page scrollable con secciones: Hero, Quienes Somos, Desarrollo de Sistemas, Impresos, Contacto
- Seccion de Desarrollo de Sistemas con casos de estudio (La Venezolana de Seguros, UbikGo/Uvic)
- Seccion de Impresos con grilla resumida de categorias de productos
- CTAs a WhatsApp Business con mensaje pre-llenado
- Responsive (desktop y mobile)
- Deploy como sitio estatico (HTML/CSS/JS) en Vercel o hosting estatico
- Estetica dark/tech alineada con DESIGN.md de Linear customizado

**No incluye:**
- Sistema de autenticacion o areas privadas
- Carrito de compras, cotizador automatico o formulario de pedido
- Backend, base de datos o API
- Integracion con CRM, email marketing o analytics
- Version en ingles
- Migracion de sitio existente
- Panel de administracion de contenido

## 4. Actores

- **Visitante corporativo**: decisor de empresa (gerente IT, director de operaciones, CEO) que evalua si Artgoritmo puede resolver su necesidad de sistema a medida o material impreso publicitario. Navega la landing, revisa los casos de estudio de sistemas, ve el catalogo de impresos, y contacta via WhatsApp o formulario.

## 5. Precondiciones

- Los assets visuales estan disponibles: screenshots de La Venezolana de Seguros (sistema de gestion de contratos/polizas, interfaz teal), screenshots y videos de UbikGo/Uvic (sistema de cotizacion de grua, interfaz azul oscuro con acentos naranja), imagenes de marca (vision, concepto, bienvenida, backing, bandolera), catalogo PDF de productos impresos
- Los textos corporativos de Vision y Concepto estan redactados
- El DESIGN.md de referencia (basado en Linear, customizado) esta disponible
- Se tiene cuenta de Vercel o hosting estatico para deploy

## 6. Disparador

- El visitante accede a la URL de la landing (link directo compartido por email, WhatsApp, o tarjeta de presentacion)

## 7. Flujo Principal

1. El visitante llega a la landing y ve el Hero: logo de Artgoritmo, headline directa sobre lo que hace la empresa, CTA principal ("Hablemos de tu proyecto")
2. Hace scroll y llega a "Quienes Somos": textos de Vision y Concepto tomados del material existente, RIF J-50209850-0
3. Continua scroll hacia "Desarrollo de Sistemas" (seccion con mayor peso visual): ve los casos de estudio presentados como cards con screenshot estilizado, nombre del cliente, descripcion del problema resuelto y features clave
4. Caso 1 — La Venezolana de Seguros y Vida: sistema que gestiona 131,555+ contratos de polizas vehiculares, con busqueda por placa, modulos de pagos/polizas/usuarios/reportes/solicitudes/configuracion/tasa BCV
5. Caso 2 — UbikGo (Uvic): plataforma para venta y operacion de polizas de grua, con cotizacion por mapa Mapbox, registro de vehiculos, contratos de servicio, canje de contrato por servicio de grua con calculo de distancia, panel admin de asignacion de grueros, cotizacion dual USD/Bs
6. Cada caso tiene un CTA secundario ("Quiero algo parecido" o "Agendar reunion")
7. Hace scroll hacia "Impresos": grilla de categorias de productos (Roll Ups, Backings, Aranas, Banderines, Stands, Bolsos, Chupetas, Cajas de Luz, Kioscos, Tazas y Gorras, Impresion) con imagen representativa de cada categoria, sin precios
8. La seccion de impresos tiene un CTA ("Solicitar presupuesto de impresos")
9. Llega a la seccion de Contacto: formulario simple (nombre, empresa, email/telefono, mensaje) o boton directo a WhatsApp Business con mensaje pre-llenado
10. El nav sticky permite saltar a cualquier seccion desde cualquier punto de la pagina

## 8. Flujos Alternativos

1. **Visitante llega desde mobile:**
   - La landing se adapta a viewport mobile con las mismas secciones en orden vertical
   - Los screenshots de sistemas se muestran a ancho completo sin mockup de laptop
   - La grilla de impresos pasa a 2 columnas o carrusel horizontal
   - El boton de WhatsApp abre la app directamente

2. **Visitante interesado solo en sistemas:**
   - Usa el nav para saltar directo a "Desarrollo de Sistemas"
   - Revisa los casos y hace clic en el CTA de cotizacion de sistemas
   - Se abre WhatsApp con mensaje pre-llenado: "Hola, me interesa cotizar un sistema a medida con Artgoritmo"

3. **Visitante interesado solo en impresos:**
   - Usa el nav para saltar directo a "Impresos"
   - Revisa las categorias y hace clic en el CTA de presupuesto de impresos
   - Se abre WhatsApp con mensaje pre-llenado: "Hola, me interesa solicitar presupuesto de impresos con Artgoritmo"

4. **Visitante que quiere mas detalle de un caso de estudio:**
   - Hace clic en la card del caso y se expande un modal o seccion inline con mas screenshots y detalle de features
   - Puede cerrar y volver al scroll normal

## 9. Reglas de Negocio

1. La seccion de Desarrollo de Sistemas SIEMPRE aparece antes que la de Impresos y ocupa mayor superficie visual (aprox 60/40)
2. Los precios de productos impresos NO se muestran en la landing — toda negociacion es via contacto directo
3. Los screenshots de sistemas se muestran con datos reales visibles (nombres de clientes en el sistema, cantidades de contratos) para demostrar que son sistemas en produccion, no mockups
4. El RIF J-50209850-0 debe aparecer visible en la landing (en el header o footer)
5. Todo el contenido esta en espanol
6. Los CTAs de WhatsApp usan el formato wa.me/[numero]?text=[mensaje-encoded] con mensajes diferenciados segun la seccion (sistemas vs impresos vs general)
7. La estetica sigue el DESIGN.md de referencia: dark canvas, tipografia geometrica/tech, acentos plateados/gris claro, cards con bordes sutiles, screenshots como hero elements
8. La landing NO usa la mascota de la bombilla del material de bienvenida — el tono es corporativo/serio
9. El logo de Artgoritmo con su tipografia geometrica caracteristica es el unico elemento de marca en el header

## 10. Suposiciones

### Funcionales
1. La landing es un sitio estatico de una sola pagina (single-page scrollable), no una web app con rutas multiples ni login. *(validada)*
2. La seccion de "Desarrollo de Sistemas" ocupa mayor peso visual y jerarquia que la seccion de "Impresos" (aprox 60/40), segun la indicacion de que los clientes target son del rubro de sistemas. *(validada)*
3. Cada sistema desarrollado (La Venezolana de Seguros, UbikGo/Uvic) se presenta como un "caso de estudio" con screenshot destacado, nombre del cliente, descripcion breve del problema resuelto, y features clave visibles en la interfaz. *(validada)*
4. Los screenshots de los sistemas se muestran como imagenes estaticas estilizadas (mockup en laptop/monitor), no como videos embebidos. *(validada)*
5. El catalogo de productos impresos se presenta como una grilla o carrusel resumido con las categorias principales (Roll Ups, Backings, Aranas, Banderines, Stands, etc.) sin mostrar precios. *(validada)*
6. La landing NO incluye un carrito de compras, cotizador automatico ni formulario de pedido — la conversion es via boton de contacto (WhatsApp o formulario simple). *(validada)*
7. La pagina de Artgoritmo actual (si existe) NO se migra; esta landing es un asset nuevo e independiente. *(validada)*

### Usuarios
8. El visitante principal es un decisor corporativo (gerente de IT, director de operaciones, CEO de aseguradora o empresa mediana) que evalua si Artgoritmo puede resolver su necesidad de sistema o material impreso. *(validada)*
9. No hay roles autenticados ni areas privadas. Todo el contenido es publico. *(validada)*
10. El CTA principal para sistemas es "Solicitar cotizacion" o "Agendar reunion", y para impresos es "Ver catalogo" o "Solicitar presupuesto" — ambos llevan a WhatsApp o formulario. *(validada)*

### Datos
11. El contenido de Vision, Concepto y textos corporativos se toma directamente de las imagenes suministradas (J-50209850-0, textos de vision y concepto ya redactados). *(validada)*
12. La landing incluye las secciones: Hero, Quienes Somos (mision/vision/concepto), Desarrollo de Sistemas (casos), Impresos (catalogo resumido), Contacto/CTA. *(validada)*
13. Los textos se muestran en espanol. No hay version en ingles. *(validada)*
14. La mascota/personaje de la bombilla (del material de bienvenida) NO se usa en la landing corporativa — el tono es profesional/serio para el target de decisores corporativos. *(validada)*

### Permisos
15. No aplica — no hay sistema de autenticacion ni roles. *(validada)*

### Integraciones
16. El formulario de contacto envia a WhatsApp Business via link directo (wa.me) con mensaje pre-llenado, no requiere backend ni base de datos. *(validada)*
17. La landing se despliega como sitio estatico (HTML/CSS/JS) compatible con Vercel o cualquier hosting estatico. *(validada)*
18. No se integra con CRM, email marketing ni analytics en esta primera version. *(validada)*

## 11. Criterios de Aceptacion

1. Dado que el visitante accede a la URL, cuando la pagina carga, entonces ve el Hero con logo de Artgoritmo, headline de posicionamiento y CTA principal visible above the fold.
2. Dado que el visitante hace scroll, cuando pasa el Hero, entonces encuentra la seccion "Quienes Somos" con textos de Vision y Concepto coherentes con el material de marca existente.
3. Dado que el visitante llega a la seccion de Desarrollo de Sistemas, cuando la visualiza, entonces esta seccion ocupa mayor superficie visual que la de Impresos y aparece primero en el orden de scroll.
4. Dado que el visitante ve un caso de estudio de sistema, cuando observa la card, entonces puede identificar: nombre del cliente, screenshot del sistema, descripcion del problema resuelto y features clave.
5. Dado que el visitante ve el caso de La Venezolana de Seguros, cuando lee el contenido, entonces identifica que es un sistema de gestion de contratos/polizas en produccion con datos reales visibles.
6. Dado que el visitante ve el caso de UbikGo, cuando lee el contenido, entonces identifica que es una plataforma de polizas de grua con cotizacion por mapa, gestion de vehiculos y contratos.
7. Dado que el visitante llega a la seccion de Impresos, cuando la visualiza, entonces ve una grilla con las categorias principales de productos sin precios visibles.
8. Dado que el visitante hace clic en un CTA de sistemas, cuando se ejecuta la accion, entonces se abre WhatsApp con un mensaje pre-llenado diferenciado para sistemas.
9. Dado que el visitante hace clic en un CTA de impresos, cuando se ejecuta la accion, entonces se abre WhatsApp con un mensaje pre-llenado diferenciado para impresos.
10. Dado que el visitante navega desde un dispositivo mobile, cuando ve la landing, entonces todas las secciones se adaptan correctamente al viewport sin contenido cortado ni overflow horizontal.
11. Dado que el visitante usa el nav sticky, cuando hace clic en un enlace de seccion, entonces el scroll lo lleva suavemente a la seccion correspondiente.
12. Dado que la landing esta desplegada, cuando se inspecciona el footer o header, entonces el RIF J-50209850-0 es visible.
13. Dado que la landing usa la estetica definida, cuando se visualiza, entonces el fondo es oscuro, la tipografia es geometrica/tech, los acentos son plateados/gris claro, y las cards tienen bordes sutiles — alineado con el DESIGN.md de referencia.

## 12. BDD / Gherkin

```gherkin
# language: es
Caracteristica: Landing corporativa Artgoritmo
  Como visitante corporativo
  Quiero conocer los servicios de Artgoritmo (sistemas y impresos)
  Para evaluar si son el proveedor adecuado y contactarlos

  Escenario: Carga inicial de la landing
    Dado que accedo a la URL de la landing
    Cuando la pagina termina de cargar
    Entonces veo el logo de Artgoritmo en el header
    Y veo un headline de posicionamiento
    Y veo un CTA principal visible sin hacer scroll

  Escenario: Navegacion por secciones via nav sticky
    Dado que estoy en cualquier punto de la landing
    Cuando hago clic en "Desarrollo de Sistemas" en el nav
    Entonces el scroll me lleva suavemente a la seccion de sistemas

  Escenario: Visualizacion de caso de estudio - La Venezolana
    Dado que estoy en la seccion de Desarrollo de Sistemas
    Cuando veo la card de La Venezolana de Seguros
    Entonces puedo ver un screenshot del sistema con datos reales
    Y una descripcion del problema resuelto
    Y las features clave del sistema
    Y un CTA para solicitar cotizacion

  Escenario: Visualizacion de caso de estudio - UbikGo
    Dado que estoy en la seccion de Desarrollo de Sistemas
    Cuando veo la card de UbikGo
    Entonces puedo ver un screenshot del sistema con interfaz azul
    Y una descripcion de la plataforma de polizas de grua
    Y las features clave incluyendo cotizacion con mapa
    Y un CTA para solicitar cotizacion

  Escenario: Contacto via WhatsApp para sistemas
    Dado que estoy en la seccion de Desarrollo de Sistemas
    Cuando hago clic en "Solicitar cotizacion de sistema"
    Entonces se abre WhatsApp con mensaje pre-llenado sobre sistemas

  Escenario: Contacto via WhatsApp para impresos
    Dado que estoy en la seccion de Impresos
    Cuando hago clic en "Solicitar presupuesto de impresos"
    Entonces se abre WhatsApp con mensaje pre-llenado sobre impresos

  Escenario: Visualizacion en mobile
    Dado que accedo a la landing desde un dispositivo mobile
    Cuando navego por todas las secciones
    Entonces el contenido se adapta al viewport sin overflow horizontal
    Y los screenshots de sistemas se muestran a ancho completo
    Y el boton de WhatsApp abre la app directamente

  Escenario: Grilla de productos impresos
    Dado que estoy en la seccion de Impresos
    Cuando veo la grilla de categorias
    Entonces veo al menos 8 categorias con imagen representativa
    Y ninguna categoria muestra precio
```

## 13. Wireframes ASCII

### Pantalla: Landing completa (desktop)

```
+================================================================+
| [Logo Artgoritmo]    Nosotros  Sistemas  Impresos  Contacto   |
|                                              [Hablemos]        |
+================================================================+

+----------------------------------------------------------------+
|                                                                |
|              CONSTRUIMOS SOFTWARE                              |
|              Y LO IMPRIMIMOS TAMBIEN                           |
|                                                                |
|              Sistemas a medida para aseguradoras               |
|              y empresas. Impresos para todo lo demas.          |
|                                                                |
|              [ Hablemos de tu proyecto ]                       |
|                                                                |
|              J-50209850-0                                      |
+----------------------------------------------------------------+

+----------------------------------------------------------------+
|  QUIENES SOMOS                                                 |
|                                                                |
|  +---------------------------+  +---------------------------+  |
|  | VISION                    |  | CONCEPTO                  |  |
|  |                           |  |                           |  |
|  | Llevamos anos en esto.    |  | No somos una agencia de   |  |
|  | Sistemas, imprenta,       |  | publicidad. Armamos los   |  |
|  | produccion: cambiamos     |  | sistemas que hacen que    |  |
|  | de herramientas cuando    |  | el negocio del cliente    |  |
|  | el mercado lo pide,       |  | funcione. Cada proyecto   |  |
|  | pero la idea es la        |  | sale distinto al          |  |
|  | misma — crecer junto      |  | anterior porque cada      |  |
|  | al cliente.               |  | cliente es distinto.      |  |
|  +---------------------------+  +---------------------------+  |
+----------------------------------------------------------------+

+----------------------------------------------------------------+
|  SISTEMAS                                                      |
|  Lo que hemos construido                                       |
|                                                                |
|  +----------------------------------------------------------+  |
|  | [Screenshot La Venezolana - mockup laptop]                |  |
|  |                                                          |  |
|  |  La Venezolana de Seguros y Vida                         |  |
|  |                                                          |  |
|  |  Les hicimos el sistema donde gestionan todas sus        |  |
|  |  polizas vehiculares. Hoy corre con 131,555 contratos.  |  |
|  |                                                          |  |
|  |  - Busqueda por placa en segundos                        |  |
|  |  - Pagos, polizas, reportes, tasa BCV                   |  |
|  |  - Estadisticas con filtros por periodo y vendedor       |  |
|  |                                                          |  |
|  |  [ Quiero algo parecido ]                                |  |
|  +----------------------------------------------------------+  |
|                                                                |
|  +----------------------------------------------------------+  |
|  | [Screenshot UbikGo - mockup laptop]                      |  |
|  |                                                          |  |
|  |  UbikGo                                                  |  |
|  |                                                          |  |
|  |  Plataforma para vender y operar polizas de grua.        |  |
|  |  Desde la cotizacion hasta la asignacion del gruero.     |  |
|  |                                                          |  |
|  |  - Cotizacion con mapa, calcula distancia en vivo        |  |
|  |  - Registro de vehiculos con placa, marca, modelo        |  |
|  |  - Contratos anuales con servicios restantes             |  |
|  |  - Panel de asignacion de grueros                        |  |
|  |  - Precios en USD y Bs                                   |  |
|  |                                                          |  |
|  |  [ Quiero algo parecido ]                                |  |
|  +----------------------------------------------------------+  |
+----------------------------------------------------------------+

+----------------------------------------------------------------+
|  IMPRESOS                                                      |
|  Tambien hacemos esto                                          |
|                                                                |
|  +----------+  +----------+  +----------+  +----------+       |
|  | [img]    |  | [img]    |  | [img]    |  | [img]    |       |
|  | Roll Ups |  | Backings |  | Aranas   |  |Banderines|       |
|  +----------+  +----------+  +----------+  +----------+       |
|                                                                |
|  [ Ver catalogo completo ]                                     |
|  [ Pedir presupuesto ]                                         |
+----------------------------------------------------------------+

+----------------------------------------------------------------+
|  HABLEMOS                                                      |
|                                                                |
|  Nombre                                                        |
|  [___________________________________________]                 |
|                                                                |
|  Empresa                                                       |
|  [___________________________________________]                 |
|                                                                |
|  Email o Telefono                                              |
|  [___________________________________________]                 |
|                                                                |
|  Que necesitas?                                                |
|  [___________________________________________]                 |
|  [___________________________________________]                 |
|                                                                |
|  [ Enviar ]              [ Escribir por WhatsApp ]             |
+----------------------------------------------------------------+

+----------------------------------------------------------------+
|  [Logo Artgoritmo]   J-50209850-0                              |
|  Caracas, Venezuela                                            |
|  2026 Grupo Artgoritmo                                         |
+----------------------------------------------------------------+
```

Nota: El nav es sticky. Los screenshots de sistemas van en cards con bordes sutiles (1px inset) sobre fondo oscuro, dentro de mockups de laptop/monitor. La seccion de Sistemas usa cards grandes (full-width o split text+screenshot). Impresos usa grilla compacta con solo 4 categorias destacadas + boton al catalogo HTML externo.
