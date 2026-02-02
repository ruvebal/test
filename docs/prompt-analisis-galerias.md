Prompt (usuario):

Teniendo en cuenta mis líneas de diseño y decisiones técnicas descritas en `project-brief.md` y `project-inspiration.md` (y respetando los tokens de `assets/css/_variables.css`), analiza estos 3 portfolios de ilustradores - https://www.sileent.com/
- https://griflan.com/
- https://www.chanel.com/es/joyeria/coco-crush-encuentros/

## Volcado de entrega (archivos destino)

- `docs/prompt-analisis-galerias.md`: pega este prompt + la respuesta completa.
- `project-inspiration.md`: añade las 3 URLs analizadas y 3 bullets de “patrones transferibles” (sin copiar).
- `project-brief.md`: incorpora 2 decisiones concretas (layout + contenido) en Key Sections / Design Direction.

Objetivo pedagógico: detectar **patrones transferibles** (no copiar estética).

Para cada uno, evalúa:

1. **Diseño Visual (Awwwards criteria)**

   - Estética general (1-10)
   - Tipografía y jerarquía
   - Uso de color y contraste
   - Composición y espaciado

2. **UX de Galería**

   - Facilidad para explorar proyectos
   - Claridad de navegación
   - Información por proyecto (título, descripción, tags)
   - Call-to-actions efectivos

3. **Técnica**

   - Tipo de layout (grid, masonry, custom)
   - Responsive behavior
   - Performance (carga de imágenes)
   - Micro-interacciones

4. **Insights Accionables (aplicables a mi brief)**
   - 3 patrones que puedo reutilizar sin copiar (con explicación)
   - 3 riesgos/antipatrones a evitar (con explicación)
   - 2 decisiones concretas para mi galería (layout + contenido), justificadas con mi `project-brief.md`

Devuelve:

- Tabla comparativa (Diseño / UX / Técnica)
- “Decisiones para mi proyecto” (bullets)
- Checklist de verificación (qué revisar al implementarlo)

---

Respuesta (análisis):

Resumen ejecutivo

Analizo los tres sitios solicitados —Sileent, Griflan, y la sección de Coco Crush de Chanel— enfocándome en diseño visual, experiencia de usuario en la galería y aspectos técnicos. Extraigo patrones transferibles y riesgos para aplicar al proyecto descrito en `project-brief.md` y `project-inspiration.md`. Donde propongo colores o tokens, indico que debes mapearlos a los tokens en `assets/css/_variables.css`.

Análisis por sitio

1) https://www.sileent.com/

Diseño Visual (Awwwards criteria)
- Estética general: 8/10 — Minimalismo ilustrativo con buen uso de espacio negativo y micro‑detalles.
- Tipografía y jerarquía: tipografía moderna, buena escala entre título y cuerpo; jerarquía clara.
- Uso de color y contraste: paleta sobria con acentos; contraste suficiente en la mayoría de secciones.
- Composición y espaciado: generoso whitespace; composiciones centradas y alineadas que dejan respirar el trabajo visual.

UX de Galería
- Facilidad para explorar proyectos: alta — navegación por tarjetas grandes y scroll continuo.
- Claridad de navegación: simple y directa; menú minimalista y breadcrumbs en páginas internas.
- Información por proyecto: muestra título y una breve categoría; algunas piezas carecen de metadatos extensos.
- Call-to-actions efectivos: CTAs discretos (ver proyecto, contacto), bien posicionados pero no agresivos.

Técnica
- Tipo de layout: grid con cards grandes; parece un grid CSS clásico con filas uniformes.
- Responsive behavior: fluido; en móvil las tarjetas apilan y mantienen ritmo visual.
- Performance: imágenes optimizadas pero algunas hero images pesan; lazy-loading aplicado en galerías.
- Micro-interacciones: transiciones suaves en hover y entrada de elementos (fade/translate).

Insights accionables (Sileent)
- 3 patrones reutilizables:
  1. Tarjetas grandes con foco visual central: prioriza la imagen del proyecto y usa un pequeño overlay para metadatos.
  2. Navegación mínima + foco en contenido: menú compacto y dejar que el trabajo llame la atención.
  3. Lazy-loading progresivo con placeholders neutros: mantiene la sensación de performance.
- 3 riesgos/antipatrones:
  1. Falta de metadatos en tarjeta inicial — obliga a abrir proyecto para saber qué es.
  2. Hero images pesadas sin variantes WebP/AVIF.
  3. Dependencia de hover para revelar información (no es accesible en touch sin alternativa).
- 2 decisiones concretas para mi galería (justificación con project-brief):
  1. Layout: Grid responsivo con cards grandes y relación de aspecto fija; justificación: coincide con la estrategia desktop-first y permite escala tipográfica clara.
  2. Contenido: Mostrar título, año y 2 tags en la tarjeta + ficha detalle con proceso; justificación: balance entre limpieza (accesibilidad) y contexto para clientes.

---

2) https://griflan.com/

Diseño Visual (Awwwards criteria)
- Estética general: 7/10 — estética ilustrativa colorida, más experimental.
- Tipografía y jerarquía: tipografías audaces en títulos; jerarquía a veces compite con los elementos gráficos.
- Uso de color y contraste: paleta viva; buen contraste en CTA pero algunas áreas muy saturadas.
- Composición y espaciado: composiciones dinámicas, menos whitespace; sensación más comprimida que Sileent.

UX de Galería
- Facilidad para explorar proyectos: moderada — requiere más atención para localizar proyectos por diseño más “artístico”.
- Claridad de navegación: navegación creativa, a veces expectante; puede confundir usuarios que buscan rapidez.
- Información por proyecto: títulos y tags presentes, pero no siempre consistentes.
- Call-to-actions efectivos: CTAs integrados en la experiencia visual, visibles pero no convencionales.

Técnica
- Tipo de layout: mezcla de grid con secciones a medida; composiciones asimétricas.
- Responsive behavior: adaptaciones creativas; en móvil se simplifica correctamente.
- Performance: depende de animaciones y sprites SVG; imagenes optimizadas en varios casos.
- Micro-interactions: interacciones ricas (hover, parallax leve, micro-movimiento en ilustraciones).

Insights accionables (Griflan)
- 3 patrones reutilizables:
  1. Ritmo visual con combinaciones asimétricas: alternar tarjetas alineadas y tarjetas full-bleed para crear ritmo.
  2. Integración de tags/roles sobre la imagen con alto contraste para contexto inmediato.
  3. Uso de micro‑movimientos para enfatizar intención (p.ej. slight parallax) sin saturar la experiencia.
- 3 riesgos/antipatrones:
  1. Diseño demasiado experimental compromete claridad — sacrifica escaneabilidad.
  2. Colores muy saturados pueden romper la jerarquía tipográfica.
  3. Dependencia de animaciones para comunicar estructura; si JS falla, la UX cae.
- 2 decisiones concretas para mi galería:
  1. Layout: Alternar módulos grid + full-bleed para proyectos destacados; justificación: permite destacar piezas clave si quieres mostrar trabajos heroicos sin perder coherencia.
  2. Contenido: Incluir tags y rol visibles en la tarjeta; justificación: facilita filtrado mental y comunicación rápida al visitante.

---

3) https://www.chanel.com/es/joyeria/coco-crush-encuentros/

Diseño Visual (Awwwards criteria)
- Estética general: 9/10 — producción editorial, lujo, fotografía de alta calidad.
- Tipografía y jerarquía: tipografía sobria y elegante; jerarquía clara y refinada.
- Uso de color y contraste: paleta neutra con acentos metálicos; contraste muy controlado.
- Composición y espaciado: diseño editorial con mucha respiración y grid preciso.

UX de Galería
- Facilidad para explorar proyectos: alta — navegación editorial clara, filtros y secciones dedicadas.
- Claridad de navegación: excelente; uso de secciones, breadcrumbs y CTA claros.
- Información por proyecto: completa (título, pieza, contexto, llamada a acción comercial).
- Call-to-actions efectivos: CTAs enfocados a conversión (ver detalle, comprar, compartir) integrados sin romper estética.

Técnica
- Tipo de layout: layout editorial a base de grid, con módulos de ancho variable y hero sections.
- Responsive behavior: altamente pulido; ajustes tipográficos y espaciales en cada breakpoint.
- Performance: buenas prácticas (formatos modernos, imágenes optimizadas, placeholders), aunque recursos de marca (fonts, vídeos) aumentan coste.
- Micro-interactions: sutiles, enfocados en elegancia (transiciones suaves, hover elegante, desplazamiento controlado).

Insights accionables (Chanel)
- 3 patrones reutilizables:
  1. Grid editorial con módulos de ancho variable para jerarquizar proyectos.
  2. Fichas de proyecto ricas en contexto (texto + fotografía + CTA) sin perder elegancia.
  3. Uso de tipografía y espaciado como elemento de marca; tipografía cuidada mejora percepción profesional.
- 3 riesgos/antipatrones:
  1. Producción pesada: fotos de alta resolución y vídeo pueden penalizar performance si no se gestionan.
  2. Exceso de recursos de marca (webfonts pesadas) sin fallback optimizado.
  3. Complejidad editorial que requiere mantenimiento; si tu proyecto es pequeño, puede sobrecargarte.
- 2 decisiones concretas para mi galería:
  1. Layout: Grid editorial con módulos variables para destacar 2-3 proyectos hero en la home; justificación: alinea con objetivo de mostrar trabajos clave y mantiene escala tipográfica (importante en brief).
  2. Contenido: Ficha de proyecto con 1 hero, 3 imágenes de proceso, rol y breve case study; justificación: proporciona contexto relevante a clientes y respalda objetivos de accesibilidad y contenido completo.

---

Tabla comparativa (Diseño / UX / Técnica)

| Sitio | Diseño (estética / tipografía / color) | UX Galería (explorar / nav / info) | Técnica (layout / responsive / perf / micro) |
|---|---:|---:|---|
| Sileent | 8 — minimalista, buena jerarquía, paleta sobria | Alta — tarjetas grandes, navegación simple, metadata limitada | Grid clásico / buena / lazy-loading / transiciones suaves |
| Griflan | 7 — colorido, experimental, jerarquía variable | Media — más artístico, navegación creativa pero menos escaneable | Grid + módulos / adaptativo / depende de animaciones / micro-movimientos |
| Chanel (Coco Crush) | 9 — editorial, tipografía refinada, paleta neutra | Muy alta — editorial y comercial, info completa, CTAs claros | Grid editorial / excelente / formatos optimizados / micro-interacciones sutiles |


Decisiones para mi proyecto (resumen ejecutable)

- Layout: Usar un grid responsivo CSS Grid como base con dos variantes: tarjetas grandes uniformes para catálogo y módulos full-bleed/hero para 2-3 proyectos destacados. Implementar relación de aspecto fija en las cards para consistencia visual.
- Contenido por tarjeta: título, año, 1-2 tags (rol/technique), y un breve snippet (máx 1 línea). En la ficha detalle: hero, 3 imágenes de proceso optimizadas, párrafo de 50-80 palabras sobre el proyecto, lista de roles/técnicas y botón claro de contacto/descarga.
- Accesibilidad y tokens: mapear colores y espacios a `assets/css/_variables.css`, garantizar contraste WCAG AA, añadir alt y roles ARIA, y soportar navegación por teclado.

Checklist de verificación (qué revisar al implementarlo)

1. Tokens
   - Mapeo de colores y espaciados a `assets/css/_variables.css`.
2. Layout & Grid
   - CSS Grid con fallback flexbox para navegadores antiguos.
   - Relación de aspecto fija en cards + object-fit para imágenes.
3. Imágenes & Performance
   - Generar WebP/AVIF + srcset para imágenes.
   - Implementar lazy-loading nativa (loading=lazy) y placeholders (LQIP o dominant color).
   - Verificar Lighthouse (target >= 90 en Performance durante desarrollo).
4. Accesibilidad
   - Estructura semántica (section, article, figure, figcaption).
   - Teclado: focus states claros y controlables.
   - ARIA roles solo donde sean necesarios.
   - Contraste de texto >= 4.5:1 para body text.
5. Interacciones
   - Preferencias reduced-motion respetadas.
   - Micro-interacciones con transform/opacity (GPU friendly).
6. Contenido & SEO
   - Cada proyecto con H1/H2 claro en su página, meta description y Open Graph.
7. Testing
   - Probar en móvil, tablet y desktop; comprobar performance en conexiones lentas.
   - Tests de navegación con teclado y lector de pantalla básicos.


Notas finales

- Prioriza legibilidad y performance sobre efectos excesivos. Toma elementos de Sileent (simplicidad), Griflan (ritmo visual) y Chanel (cuidado editorial) y combínalos en un sistema coherente usando tokens y design system.
- Evita depender exclusivamente de hover o animaciones para comunicar información clave.

---

Fin del análisis.
