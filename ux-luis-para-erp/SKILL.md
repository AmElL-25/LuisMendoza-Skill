---
name: UX Luis para ERP
description: >-
  Úsala al crear, auditar o mejorar cualquier pantalla de cualquier módulo de un
  ERP o CRM comercial, para que sea simple, clara y fácil de usar sin pensar.
---
# UX Luis para ERP

**La única pregunta:** ¿alguien que entra por primera vez entiende en 5 segundos qué es esta pantalla y qué hacer? Si tiene que pensar, el diseño falló.

**La vara de calidad:** cada pantalla debe sentirse al nivel de los productos de Apple y Google: simple, pulida, consistente y rápida. Si algo se ve "casi bien", todavía no está listo.

**Si dos reglas chocan, gana la de más arriba:**
1. Que el usuario no pierda datos ni dinero (acciones peligrosas, errores).
2. Que entienda dónde está y qué hacer (claridad y navegación).
3. Que vea lo esencial sin scroll horizontal.
4. Que se vea pulido y consistente.

**Responsive siempre:** toda regla de esta skill y todo cambio que se haga debe funcionar y verse bien en escritorio, tablet y móvil. Nada se da por terminado si solo se probó en un tamaño.

---

## Capa 1 · Las 10 reglas de oro (innegociables)

1. **Se explica sola.** Título igual al nombre del menú, nombres y botones obvios ("Registrar venta", no "Procesar").
2. **Un solo botón principal (CTA)** en la cabecera, en 1 línea con el título y las sub-vistas. Nunca dos botones que hagan lo mismo.
3. **Se escanea en 1 segundo.** Jerarquía visual clara; cada fila muestra lo esencial y 1 sola acción.
4. **Mismas convenciones en todo el ERP.** Mismos componentes, íconos conocidos y el mismo color para el mismo estado.
5. **Cero ruido.** Nada de banners, ayuda obvia, alertas fijas, "próximamente", ni automatizaciones o configuración en pantallas operativas. Nada de elementos que repiten lo que ya muestra la barra lateral ni botones que no hacen nada.
6. **Navegación estable.** Cabecera fija arriba, barra lateral fija, submenús que empujan y nunca tapan, migas de pan clicables.
7. **Sin scroll horizontal.** El contenido se encoge y compacta hasta un ancho mínimo legible; por debajo, cambia de vista.
8. **Todo el ancho y responsive siempre.** `w-full`, mobile first, probado en escritorio, tablet y móvil; chats y Kanban a pantalla completa (`100dvh`).
9. **Respeta la paciencia del usuario.** No esconder montos, estados ni fechas; errores junto al campo con la solución; siempre poder deshacer; escaneo con IA como Paso 1 cuando hay comprobante.
10. **Calidad nivel Apple y Google.** Espaciado exacto, todos los estados diseñados, respuesta inmediata y uso completo con teclado.

---

## Capa 2 · Reglas por componente

### Cabecera y navegación (igual en TODOS los módulos del sistema)
**Barra superior**
- Fija arriba, a todo el ancho: logo, luego migas de pan, luego controles a la derecha.
- Nunca se mueve, no cambia de altura y nada la tapa ni la oscurece.

**Migas de pan**
- Van justo después del logo, siempre en el mismo lugar.
- Cada parte va en negrita y es clicable, excepto la página actual, que va como texto normal.
- Sin segmentos repetidos (nada de "Inicio › Inicio") ni menús desplegables.
- En escritorio, el clic en un módulo o sección abre el panel de ese módulo con esa sección desplegada, sin cambiar de pantalla. Si el panel ya está abierto, no se cierra.
- Nombres iguales al menú. Si son largos, "…" con tooltip.

**Barra lateral**
- Siempre visible y con sus nombres. Nunca se pliega, se borra ni se mueve sola.
- En escritorio muestra solo los módulos, sin desplegarse. Nunca dos listas a la vez.
- Clic en un módulo abre su panel sin navegar. Otro clic en el mismo lo cierra y clic en otro lo cambia de inmediato.
- Solo un módulo resaltado a la vez: el del panel abierto o, sin panel, el de la pantalla actual.
- Todos los módulos se comportan igual, tengan 2 o 20 opciones.
- Orden por uso: los módulos del día a día arriba y los ocasionales (Configuración, Ayuda) al final; dentro del panel, lo más usado primero. El orden nunca cambia solo.

**Panel del módulo (escritorio)**
- Se abre al costado de la barra lateral, debajo de la barra superior, y empuja el contenido. No tapa nada ni oscurece el fondo.
- No tiene cabecera propia.
- Al elegir una opción, navega y el panel sigue abierto con esa opción resaltada.
- Se cierra con otro clic en el módulo, con Esc o con un clic en el contenido.
- Ancho ajustado al texto más largo del módulo, entre unos 200 y 264 px. Solo cambia al pasar a otro módulo.

**Secciones dentro del panel**
- Una sección con varias pantallas es un título clicable con flechita: apunta a la derecha cerrada y hacia abajo abierta.
- Al abrirla, sus pantallas aparecen debajo con sangría.
- Una sección de una sola pantalla es un enlace directo, sin flechita.
- Al entrar, solo está abierta la sección de la pantalla actual. Lo que el usuario abre o cierra se recuerda durante la sesión.
- El clic en el título solo abre o cierra la sección, no navega. Funciona con teclado.

**Detalles comunes**
- Una sola opción activa: si varias coinciden, se resalta la más específica.
- Flechitas del mismo tamaño en toda la navegación (unos 18 px) y con buen contraste.
- Si un botón no hace nada en un tamaño de pantalla, se oculta ahí. Por ejemplo, "plegar todo" en escritorio, donde la barra lateral no se despliega.
- En móvil y tablet, la barra lateral va en acordeón dentro de un cajón, con un módulo abierto a la vez.
- Pocas opciones a la vista: menú de acciones (⋯) con máximo 7 opciones, selector con más de 10 valores con buscador, y sección del panel con más de 7 pantallas dividida en subsecciones.

### Responsive (aplica a todo)
- Mobile first: cada pantalla, componente y cambio se diseña y prueba en escritorio, tablet y móvil (por ejemplo 1440, 1024, 768 y 390 px).
- En móvil, los submenús van en acordeón, las tablas pasan a tarjetas y el Kanban muestra una etapa a la vez; nada se corta ni se sale de la pantalla.
- Áreas táctiles cómodas en móvil (unos 44 px) y textos legibles sin hacer zoom.
- En móvil, el botón principal (Guardar, Registrar venta) queda fijo abajo, a todo el ancho y al alcance del pulgar. Las acciones peligrosas (Eliminar) van lejos de él.

### Indicadores y filtros
- Máximo 3 indicadores, como píldoras clicables que filtran ("Todos (120)", "Por cobrar (12)"), en lugar de tarjetas KPI grandes.
- Buscador y filtros en una sola barra, justo encima del listado, con filtros rápidos por etapa o estado, origen, asesor e interacción (los que apliquen).
- "Limpiar" solo si hay filtros activos, y el contador total antes de la tabla ("1,372 leads en total").

### Tablas, tarjetas y Kanban
- **Contacto:** avatar circular con iniciales, nombre limpio (nunca "(TikTok)" pegado al nombre) y teléfono en letra monoespaciada con botón para copiar.
- **Origen:** solo el logo oficial (WhatsApp, Instagram, Meta Ads, TikTok, Web, Referido, Orgánico) en un badge cuadrado redondeado, con el nombre en el tooltip.
- **Etiquetas:** píldoras compactas con punto de color ("• Seguimiento").
- **Responsable:** avatar pequeño con nombre, o "Sin asignar" en tono suave.
- **Tiempo:** relativo y corto ("hace 4 min", "ayer").
- **Acción:** un solo botón al final de la fila.
- **Sin scroll horizontal:** columnas flexibles que se reparten el ancho; al encogerse se compactan (Kanban: nombre, dato clave, 1 etiqueta, acciones como íconos, asesor como avatar; tablas: se ocultan primero las columnas secundarias, nunca nombre, estado, monto ni acción). Mínimo unos 200 px por columna; por debajo, Kanban muestra una etapa a la vez con píldoras y las tablas pasan a tarjetas. El scroll vertical sí está bien.
- **Muchos datos:** con cientos o miles de filas, usar paginación o scroll virtual, y mantener filtros y orden al volver a la lista.

### Chats
- Ocupan toda la altura y el ancho disponibles.
- La cabecera del contacto y su etapa del embudo van en una sola barra, para dar el máximo espacio a los mensajes.

### Formularios
- Si hay comprobante, el bloque "Subir captura y escanear con IA" va como Paso 1, arriba, y acepta pegar con Ctrl+V o arrastrar la imagen. Autocompleta y el usuario solo revisa y confirma.
- Muestra solo los campos que tu usuario necesita ahora: los que dependen de una elección aparecen al elegirla (por ejemplo, "N.º de operación" solo si el método es "Transferencia") y lo avanzado va en "Más opciones" cerrado. Con más de unos 7 campos visibles, agrúpalos en bloques con título o divide en pasos ("Paso 2 de 3"), sin perder lo escrito al cambiar de paso.
- Errores junto al campo, explicando cómo arreglarlo; nunca borrar lo que el usuario ya escribió.

### Acciones peligrosas y en lote
- Preferir **deshacer** ("Venta eliminada · Deshacer") antes que "¿Estás seguro?".
- Confirmar solo lo irreversible o lo que afecta dinero o a muchos registros, diciendo exactamente qué pasará ("Eliminar 12 leads"), con el botón peligroso en rojo y nunca como opción por defecto.
- Acciones en lote: casillas en las filas, y una barra con las acciones y el contador de seleccionados.

### Textos (microcopy)
- Botones con verbo y objeto ("Guardar cotización", no "OK").
- Trato de tú en todo el ERP ("Guarda tu cotización"), siempre igual.
- Moneda en soles con 2 decimales y separador de miles ("S/ 1,250.00"); fechas cortas y claras ("29 oct 2026"), en hora de Lima.
- Mensajes de vacío y error que digan qué pasó y qué hacer después.

### Calidad nivel Apple y Google
- **Espaciado:** una sola escala (múltiplos de 4 u 8 px) y alineaciones perfectas.
- **Estados:** cargando con esqueletos, vacío con mensaje útil y acción para empezar, error con cómo seguir, éxito con confirmación breve.
- **Respuesta inmediata:** cada clic muestra algo visible al instante (estado presionado, carga en el botón, aviso al guardar o copiar). Si tarda más de 400 ms, esqueleto o indicador de progreso; si tarda más de unos 2 segundos, di qué pasa ("Guardando venta…").
- **Se nota qué se puede tocar:** todo lo clicable (botones, píldoras, filas, enlaces) tiene hover, cursor de mano y estado presionado. Lo que no es clicable nunca parece botón ni enlace.
- **Movimiento sutil:** animaciones de paneles, menús y modales entre 150 y 300 ms (nunca más de 400 ms), que no hacen esperar, y sin saltos de diseño mientras carga.
- **Teclado y accesibilidad:** foco visible, orden lógico, Esc cierra, Enter confirma.
- **Pulido final:** íconos del mismo estilo, textos sin errores, revisado en escritorio, tablet y móvil.
- **Modo oscuro (si el ERP lo tiene):** mismos contrastes y colores de estado legibles en ambos modos.

### Tokens de diseño (usar siempre los del ERP, nunca valores sueltos)
- **Colores por estado, fijos en todo el ERP:** éxito verde, advertencia ámbar, error rojo, información azul, neutro gris; color de marca solo para el CTA principal y lo activo. Nunca solo color: sumar ícono o texto.
- **Tipografía:** máximo 3 fuentes y una escala fija de tamaños y pesos (título de página, título de sección, texto, texto secundario).
- **Forma:** los mismos radios de borde, sombras y alturas de botón e input en todo el ERP.
- Si un token no existe, proponerlo antes de inventar un valor.

---

## Capa 3 · Checklist de auditoría (puntaje sobre 10)

Cada pantalla se califica con las 10 reglas de oro: 1 punto por cada ✅. Para aprobar se necesita **9/10**, y las reglas 6 y 7 (navegación estable y sin scroll horizontal) no pueden fallar nunca.

- [ ] 1. Se explica sola
- [ ] 2. Un solo CTA, sin botones repetidos
- [ ] 3. Se escanea en 1 segundo
- [ ] 4. Mismas convenciones
- [ ] 5. Cero ruido
- [ ] 6. Navegación estable
- [ ] 7. Sin scroll horizontal (medido a 1440, 1280, 1024 y 390 px)
- [ ] 8. Todo el ancho y responsive siempre (probado en escritorio, tablet y móvil)
- [ ] 9. Respeta la paciencia del usuario (formularios largos por pasos o bloques, campos que aparecen cuando hacen falta)
- [ ] 10. Calidad nivel Apple y Google (respuesta visible en menos de 400 ms, animaciones de 300 ms o menos, lo clicable parece clicable)

## Cómo se usa

1. **Auditar:** pasar el checklist con ✅ o ❌, dar el puntaje y anotar los 3 problemas que más frenan al usuario. Explicar cada ❌ con los fundamentos de diseño.
2. **Proponer:** un cambio concreto por cada ❌, sin tocar nada todavía.
3. **Aplicar solo con aprobación:** pantalla por pantalla, en una rama aparte, sin commit, push ni deploy hasta que el dueño apruebe. Siempre con capturas del antes y el después (en escritorio y móvil) y el puntaje antes y después.
4. **Probar con 3 personas reales:** pedirles la tarea principal, observarlas sin ayudar y corregir los 3 problemas que más se repitan.

## Fundamentos de diseño (para explicar el porqué)

- **Composición:** balance, contraste, alineación, proximidad, repetición y espacio para respirar.
- **Accesibilidad:** contraste suficiente, nunca depender solo del color y textos descriptivos en botones, íconos e imágenes.
- **Color:** paleta reducida, cada color con una función.
- **Tipografía:** legible, con tamaños y pesos que marquen la jerarquía.
- **Grillas:** mobile first y un sistema de columnas para alinear todo.
- **Componentes:** CTA primario, secundario y terciario bien diferenciados y reutilizables.
- **Pantallas o módulos nuevos:** definir el objetivo y quién la usa, dibujar el flujo (con pantallas de error y confirmación) y validar un wireframe simple sin colores antes de diseñar.
