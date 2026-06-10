# clasemaestra — Business Plan Completo
**v3 · Junio 2026 · Confidencial · Quadrant Agency**

---

## Índice

1. [Resumen ejecutivo](#1-resumen-ejecutivo)
2. [Mercado](#2-mercado)
3. [Competencia](#3-competencia)
4. [Foso competitivo](#4-foso-competitivo)
5. [Producto y arquitectura](#5-producto-y-arquitectura)
6. [Pricing y entregables](#6-pricing-y-entregables)
7. [Sistema drip y bonos estacionales](#7-sistema-drip-y-bonos-estacionales)
8. [Upsell y add-ons](#8-upsell-y-add-ons)
9. [Lanzamiento — Junio 2026](#9-lanzamiento--junio-2026)
10. [Go to market](#10-go-to-market)
11. [Modelo financiero — 36 meses](#11-modelo-financiero--36-meses)
12. [Operación y stack tecnológico](#12-operación-y-stack-tecnológico)
13. [Pipeline de contenido — 5 agentes Claude](#13-pipeline-de-contenido--5-agentes-claude)
14. [Roadmap](#14-roadmap)
15. [Riesgos y mitigación](#15-riesgos-y-mitigación)
16. [Pendientes críticos antes de producción](#16-pendientes-críticos-antes-de-producción)

---

## 1. Resumen ejecutivo

**clasemaestra** es un SaaS de suscripción digital mensual para maestras de preescolar y primaria privada en México. Entrega planes de clase listos, alineados a la Nueva Escuela Mexicana (NEM 2022), organizados por grado y campo formativo, directamente en plataforma.

**Lanzamiento:** Junio 2026 vía pasarela integrada (Stripe/Conekta) (landing externa) con migración futura a stack propio.

**Audiencia:** Maestras de escuelas privadas que se identifican como "miss", no "profe". Preescolar y primaria. Digitalmente activas. Con apetito por materiales de calidad y poco tiempo.

**Posicionamiento:** Pedagogía de vanguardia (project-based learning, STEAM, socioemocional, habilidades siglo XXI). La alineación NEM 2022 es el piso, no el techo.

**Sin referencias a IA en comunicación pública.** El posicionamiento consumer es siempre *"creado y revisado por expertos en educación"*. Kipi (mascota robot con birrete) es mascota visual únicamente — nunca se presenta como "el agente que trabaja por ti". La IA se puede mencionar en documentos internos y de inversión, pero nunca en el marketing al consumidor.

### Métricas objetivo

| Indicador | Valor |
|---|---|
| Maestras objetivo México | 158,000 |
| Inversión total | $66,500 MXN |
| Breakeven | Mes 6 (Noviembre 2026) |
| Utilidad Mes 16 | $250,000 MXN/mes |
| ROI a 36 meses | 213x |
| LTV (ARPU maduro $314, churn 15%) | $1,947 MXN |
| LTV:CAC | 9.7x |

---

## 2. Mercado

México tiene más de 158,000 maestras de preescolar y primaria en escuelas privadas. Todas preparan material cada semana. El promedio es 12 horas semanales de preparación. No existe ninguna suscripción curada, en español, alineada a NEM 2022.

### TAM · SAM · SOM

| Nivel | Definición | Tamaño | Revenue potencial |
|---|---|---|---|
| TAM | Maestras preescolar + primaria privada MX + LATAM | ~650K | $193M MXN/mes |
| SAM | Maestras México digitalmente activas | ~95K | $28M MXN/mes |
| SOM | Target realista año 1–3 (1–2% del SAM) | 950–1,900 | $282K–$564K MXN/mes |

### El problema real

Las maestras de escuela privada tienen presión doble: la SEP les exige NEM 2022 (plan 2022, nomenclatura nueva, campos formativos) y los padres les exigen materiales vistosos y pedagógicamente sólidos. La mayoría sigue usando recursos de Pinterest y grupos de Facebook que aún están alineados al plan 2011. El tiempo de preparación es el recurso más escaso de cualquier docente.

### Timing

La NEM 2022 entró en vigor con poca capacitación. La mayoría de recursos gratuitos existentes todavía usan el plan anterior. clasemaestra nace alineada a la NEM desde el primer día — esa es su ventaja técnica real frente a todo el contenido gratuito existente.

---

## 3. Competencia

| Competidor | Tipo | Alineación NEM | Organización | Calidad | Precio | Entrega |
|---|---|---|---|---|---|---|
| Pinterest / Facebook grupos | UGC gratuito | ✗ Plan 2011 | Por búsqueda | Variable | Gratis | Manual |
| YouTube (tutoriales) | Video educativo | ✗ Mayoría desactualizada | Por tema | Variable | Gratis | No imprimible |
| ChatGPT / Claude directo | IA generativa | Parcial (si sabe pedir) | ✗ Sin estructura NEM | Sin data de outcome | $0–20 USD/mes | Sin comunidad · sin lock-in |
| Editoriales (Santillana, SM) | Material impreso/digital | En transición | ✓ Estructurada | Alta | $3,000–8,000/año | Paquete anual |
| SEP / AprenderEnCasa | Recurso oficial | ✓ Oficial NEM | Por grado | Genérico | Gratis | Sin personalización |
| Teachers Pay Teachers | Marketplace | ✗ Sistema anglosajón | Por búsqueda | Variable | $2–15 USD/recurso | Descarga manual |

### La brecha real del mercado

Existe contenido gratuito en abundancia y contenido caro institucional. No existe nada curado, alineado a NEM, entregado automáticamente, a precio accesible mensual.

Pero más importante: en 24 meses cualquier maestra puede pedirle planes a Claude directamente. Lo que no puede replicar es la **data de qué planes funcionan en salones reales**, su trabajo personalizado guardado en plataforma, y la comunidad de sus pares. Esos tres fosos son lo que construye clasemaestra desde el día 1 — no solo un catálogo.

---

## 4. Foso competitivo

El contenido generado con IA se comoditiza. clasemaestra no compite como catálogo de planes — compite como **el estándar validado por resultados de la enseñanza NEM**. Tres mecanismos construyen ese foso desde el día 1.

### Foso 1 — Data de outcome (rating de resultado real)

Al cerrar un plan, una sola pulsación: *"¿Funcionó en tu salón?"* — escala de estrellas 1–5 + campo opcional *"¿Qué le cambiaste?"* (una línea, cero fricción).

Esa data — qué planes realmente jalan en clase, por grado y campo formativo — **no la tiene Claude, ni ChatGPT, ni una editorial**. Solo la tiene quien observa el resultado en el salón mexicano.

La edición captura señales pasivas sin preguntar: qué secciones borran, qué agregan, cuánto tiempo pasan editando. Si el 70% de las maestras reescribe los objetivos de un plan, eso dice exactamente qué corregir en la generación — sin encuestas.

**Claim resultante:** *"los planes que miles de maestras calificaron como que sí funcionan en clase, por grado"*. Ese claim es defendible, es marketing, y alimenta la generación. Nadie más lo puede hacer.

### Foso 2 — Lock-in de plataforma (personalización como capa de datos)

Las maestras personalizan sus planes en plataforma: logo de la escuela, ajustes por grupo, notas propias. Dos efectos:

1. El trabajo guardado sube el costo de salida — irse significa rehacer todo desde cero
2. Cada edición es data pasiva que revela exactamente qué mejorar en la generación

El mensaje para la maestra es *"personaliza tus planes con tu logo y tu estilo en segundos — quedan como tuyos"*. El dato es subproducto. Nunca se vende como "te medimos".

### Foso 3 — Comunidad viva (el apego que la IA no comoditiza)

Subforos por grado. Rituales recurrentes. Un sistema de reconocimiento con currency cultural propia. El costo de salida social empieza el día 0 — antes de que la maestra use el primer plan. Tres mecanismos operan en paralelo.

#### ① Q&A en vivo mensual — ritual de retención

Sesión mensual en vivo con fecha, tema y botón "Apartar mi lugar". Apartar da +10 🌟 (ver programa de aportes). Biblioteca de grabaciones anteriores como activo permanente.

**Valor operativo:** el ritual da una razón concreta para volver cada mes — retención crítica en verano y en los primeros 90 días. La presencia del equipo respondiendo en vivo ("alguien escucha") enciende la comunidad. Las dudas que emergen en el Q&A son señal directa de qué corregir en la generación.

#### ② Programa de aportes — currency cultural 🌟

Las maestras ganan estrellitas exactamente como las dan a sus alumnos. El diseño es intencional.

**Cómo se ganan:**

| Acción | Estrellitas |
|---|---|
| Calificar un plan | +5 🌟 |
| Compartir adaptación con foto | +15 🌟 |
| Que su adaptación se cure a la biblioteca | +50 🌟 |
| Responder duda de otra maestra | +10 🌟 |
| Invitar a una colega | +40 🌟 |
| Apartar lugar en el Q&A mensual | +10 🌟 |

**Niveles con barra de progreso:**

🤝 **Aportadora** (100 🌟) → 🏆 **Destacada** (300 🌟) → 🌟 **Embajadora** (600 🌟)

**Recompensas diseñadas para NO quemar valor:**

| Recompensa | Nivel requerido | Por qué no quema valor |
|---|---|---|
| Votar el tema del próximo bundle | Aportadora | Costo $0 — genera data de demanda |
| Acceso anticipado al bundle | Aportadora | Timing, no se pierde ingreso |
| Spotlight y plantillas premium | Destacada | Estatus, costo marginal |
| 25% de comisión como afiliada | Embajadora | Auto-financiada por el referido |

**Ejemplo — Reto del mes:** *"Comparte 3 adaptaciones → bundle de julio una semana antes"*. Progreso visible: 1/3 → 2/3 → 3/3. Costo de la recompensa: timing, no ingreso perdido. Beneficio: UGC que alimenta la curaduría + data pasiva de qué funciona en clase.

#### ③ Curaduría de la comunidad → catálogo propio

Las adaptaciones destacadas se curan de vuelta a la biblioteca **con el crédito de la maestra**. Es el premio máximo — y hace crecer el catálogo desde la comunidad (no copiable) y no solo desde la IA (copiable).

Las Embajadoras son las mejores afiliadas (25% recurrente). Word of mouth en el gremio como canal primario.

### El flywheel — medible por nodo

```
Generación con IA → Personalización + uso → Data (edición + rating + Q&A)
       ↑                                              ↓
  Más maestras ← Mejor que nadie en el salón ← Generación afinada por grado
```

**KPIs por nodo:**

| Nodo | Qué mide | KPI |
|---|---|---|
| 1 — Generación + uso | Adopción del contenido | Planes descargados/mes por grado |
| 2 — Data acumulada | Fuerza del foso | Ratings + ediciones por plan/grado |
| 3 — Generación afinada | Mejora del pipeline | Score revisor NEM promedio mes a mes |
| 4 — Más maestras | Distribución orgánica | Referidas por canal comunidad vs pauta |

Cada vuelta hace la siguiente más fuerte. El competidor que entre tarde no compite contra el producto: compite contra todas las vueltas ya dadas. El programa de aportes es el acelerador que hace cada vuelta más rápida: más aportes = más data = mejor generación = más retención = más referidas.

### Fases de construcción del foso

| Fase | Qué se construye | Cuándo | Inversión |
|---|---|---|---|
| Fase A | Botón de rating + captura de descarga/re-descarga por grado. Data de outcome desde el día 1. | Lanzamiento Jun 2026 | Mínima — parte del dev actual |
| Fase B | Editor ligero en plataforma (logo, campos de texto, agregar/quitar secciones) con tracking de edición. Lock-in real. | Mes 3–4 | Dev adicional ~2 semanas |
| Fase C | La generación toma como base los patrones de edición + rating por grado. Calidad imbatible. | Mes 6+ | Iteración del pipeline existente |

### Comunidad en todos los planes — no como add-on

La comunidad es el foso que ninguna IA comoditiza. Lo primero que hace una suscriptora nueva no es bajar un PDF — es entrar al subforo de su grado. El costo de salida social empieza antes de que use el primer plan.

**Ignición de comunidad — los primeros 90 días**

Una comunidad vacía mata más que ayuda. No se activa sola. Se enciende a mano los primeros 60–90 días. Sin ignición humana, no enciende.

Tácticas:
- Sembrar con 3–5 maestras embajadoras posteando adaptaciones reales a diario los primeros 90 días (plan gratis o pago)
- Pedir específico y atado al momento: justo después de usar un plan, *"¿cómo te fue? Sube una foto de tu salón"*
- Foto primero, texto después — mucho menos fricción y genera prueba social
- Rituales recurrentes: *"Lunes de pre-clase"*, Q&A mensual en vivo, retos de temporada con progreso visible (1/3 → 2/3 → 3/3)
- Respuesta rápida y visible del equipo en cada hilo los primeros 30 días
- Activar el programa de aportes 🌟 desde el día 1: da visibilidad inmediata al sistema de reconocimiento
- Q&A en vivo programado desde el Mes 1: aunque sean 5 personas, el ritual importa más que el número

**Costo honesto:** requiere 1 persona (founder o community manager) empujándola a diario el primer trimestre. Sin este compromiso operativo, la comunidad no enciende. Presupuestarlo antes de prometérsela a las suscriptoras.

---

## 5. Producto y arquitectura

clasemaestra cubre 9 niveles de educación inicial y básica privada: 3 años de preescolar + 6 de primaria, alineados a NEM 2022. El contenido se organiza por **Campos Formativos SEP**, no por asignaturas tradicionales.

### Grados cubiertos

| Nivel | Grados | Campos formativos principales |
|---|---|---|
| Preescolar | 1°, 2°, 3° | Lenguajes, Pensamiento Matemático, Exploración del Mundo Natural, Desarrollo Personal |
| Primaria baja | 1°, 2°, 3° | Lenguajes (Español), Saberes Matemáticos, Conocimiento del Medio, Ética y Sociedad |
| Primaria alta | 4°, 5°, 6° | Lenguajes, Saberes Matemáticos, Ciencias Naturales y Tecnología, Historia, Geografía |

### Estructura de cada plan de clase

Cada plan cubre una semana completa (5 días × 45 minutos):
- **Inicio** (10 min): pregunta detonadora, activación de conocimientos previos
- **Desarrollo** (25 min): actividad principal, materiales, diferenciación para alumnos rápidos y con apoyo
- **Cierre** (10 min): reflexión, producto del alumno
- **Evaluación**: observaciones clave + rúbrica en 3 niveles (iniciado / en proceso / logrado)

Materiales siempre comunes: papel, colores, tijeras, libros de texto. Nunca tabletas, internet ni materiales costosos.

### Lo que cubre una maestra en un mes (Plan Plus)

Una maestra necesita ~80–100 sesiones planificadas por mes. El foco son las materias de mayor carga: Lenguajes y Matemáticas (60% del tiempo de preparación). Un Plan Plus entrega 48 entregables al mes para 2 grados.

### Idiomas

Tres modalidades tratadas como idioma de entrega, no como tercer idioma:
- 🇲🇽 **Español** — alineación NEM completa
- 🇺🇸 **Inglés** — adaptación pedagógica (Language Arts, Mathematics, etc.), no traducción literal
- 🌐 **Bilingüe** — cada campo en formato "ES: texto / EN: texto"

La validación del precio en inglés está planeada para Mes 6–8 vía encuesta antes de campañas específicas.

---

## 5b. Enfoques pedagógicos internacionales

clasemaestra es compatible con los marcos pedagógicos más usados en escuelas privadas de México. Lenguaje obligatorio: siempre **"compatible con"**, nunca "certificado por", "afiliado a" ni "proveedor oficial de".

| Enfoque | Aplica a | Modalidad | Qué integra |
|---|---|---|---|
| PYP (IB) | Preescolar + toda la primaria | Todos los idiomas | Indagación, conceptos transdisciplinarios, agencia del estudiante |
| CASEL (SEL) | Todos los grados | Todos los idiomas | Competencias socioemocionales en planes con campo formativo socioemocional |
| Montessori | Preescolar + primaria baja (1°–3°) | Todos los idiomas | Ambientes preparados, materiales manipulativos, aprendizaje autónomo |
| Reggio Emilia | Solo preescolar | Todos los idiomas | Proyectos emergentes, documentación pedagógica, expresión como lenguaje |
| Cambridge Framework | Todos los grados | **Solo inglés y bilingüe** | Habilidades siglo XXI, pensamiento crítico, estructura de inquiry |

> **Nota legal:** clasemaestra no es proveedor oficial ni está afiliado a IB, CASEL, Montessori, Reggio Emilia ni Cambridge Assessment. La compatibilidad se refiere a la alineación de principios pedagógicos, no a una membresía o acreditación oficial.

**Por qué esta capa importa:** Las escuelas privadas en México invierten en alinearse a marcos internacionales para diferenciarse ante los padres. clasemaestra no les obliga a elegir entre NEM y PYP/Cambridge — les da ambas cosas en el mismo plan.

---

## 6. Pricing y entregables

### Planes individuales

Precio dinámico por idioma, seleccionado al momento de suscribirse.

| Plan | 🇲🇽 ES | 🇺🇸 EN | 🌐 Bi | Entregables/mes | Incluye |
|---|---|---|---|---|---|
| **Maestra Solo** (1 grado) | $147 | $197 | $247 | 32 (20 planes + 12 materiales) | **Comunidad incluida ✓** |
| **Maestra Plus** (2 grados) | $297 | $397 | $497 | 48 (30 planes + 18 materiales) | Comunidad + bonos estacionales |
| **Grado extra Plus** | +$97 | +$127 | +$147 | — | Solo disponible en Plus |
| **Plan Escuela** (5 accesos Plus) | $997 | $1,297 | $1,597 | 48/maestra | 5 maestras eligen sus 2 grados c/u |
| **Maestra extra Escuela** | +$197 | +$257 | +$297 | — | Acceso adicional nivel Plus |

### Add-ons

| Add-on | Precio ES | Descripción |
|---|---|---|
| ~~Comunidad add-on~~ | *(eliminada — incluida en todos los planes)* | |

| Mega Bundle Anual | $1,997 one-time | Año completo de contenido |
| Pack Certificación Docente | $497 one-time | Certificación adicional |

### Programa de afiliadas

- 25% de comisión recurrente durante el primer año (ligada al nivel Embajadora del programa de aportes)
- Las maestras más activas de la comunidad son el canal principal de referido
- **50% de descuento el primer mes para la colega referida** — incentivo doble: comisión para quien refiere + reducción de fricción para quien llega
- Conectado con estatus de comunidad: visibilidad + comisión

### ARPU proyectado por mix de suscriptoras

| Período | ARPU | Mix asumido |
|---|---|---|
| Meses 4–6 | $264 | 40% Solo, 50% Plus, 10% Escuela |
| Meses 7–12 | $314 | 35% Solo, 52% Plus, 13% Escuela |
| Meses 13+ | $357 | 30% Solo, 55% Plus, 15% Escuela |

---

## 7. Sistema drip y bonos estacionales

Dos sistemas independientes en plataforma:

### Bundle mensual completo (Modelo A)

El bundle mensual completo se libera al inicio del mes, sin drip ni candados por semana. Organizado por **semana sugerida** y por los **4 campos formativos NEM**. Una suscriptora nueva accede al mes en curso más todos los meses anteriores disponibles en su biblioteca — siempre hay algo nuevo sin depender de un journey individual.

### Bonos estacionales (fecha calendario)

Se publican en fecha fija para **todas las suscriptoras activas simultáneamente**.

| Bono | Fecha de publicación |
|---|---|
| Regreso a Clases | 15 de agosto |
| Día de Muertos | 15 de octubre |
| Navidad / Posadas | 25 de noviembre |
| Semana Santa | 15 de marzo |

El drip nunca da acceso total — el modelo es de biblioteca creciente, no de catálogo completo al inicio.

---

## 8. Upsell y add-ons

El upsell no se vende activamente — sucede cuando la maestra toma más grados o necesita algo específico.

**Upsell natural:**
- Maestra Solo que quiere un segundo grado → Plus ($297 vs $147)
- Maestra Plus que toma 3er grado → +$97/mes (grado extra)
- Escuela que agrega una maestra → +$197/maestra

**Palanca estacional de upsell:**
- Agosto (regreso a clases): momento óptimo para upgrade Solo → Plus
- Enero (inicio 2° semestre): segunda oportunidad de conversión

---

## 9. Lanzamiento — Junio 2026

### Estrategia de lanzamiento

El lanzamiento es en **agosto**, directo al ciclo escolar. Es el momento de mayor necesidad de las maestras: empiezan un nuevo ciclo y necesitan materiales NEM alineados desde la primera semana. No hay venta de verano — junio y julio son de desarrollo.

**Pausa de verano** (aplica desde el segundo año): a partir de 2027, las suscriptoras activas pueden pausar jul–ago sin cobro, conservando sus planes personalizados, nivel 🌟 y acceso a la comunidad, con reanudación automática el 1 de septiembre.

### Calendario de lanzamiento

| Mes | Hito | Detalle |
|---|---|---|
| Jun 2026 | Desarrollo plataforma | Programador construye sistema propio |
| Jul 2026 | Desarrollo agentes Claude | Programador construye pipeline 5 agentes |
| Ago 2026 | **Lanzamiento** | Ciclo escolar · muestra gratis F1 · Plan Solo/Plus/Escuela · pauta $30K |
| Sep 2026 | Ciclo escolar completo | Todos los grados + pauta $30K activa |
| Nov 2026 | Breakeven | Inversión $66,500 recuperada — Mes 6 |

### Mecánica de conversión

- **Muestra gratis** (lead magnet F1): un plan completo descargable sin crear cuenta, a cambio de email. Entrada al funnel sin riesgo de abuso de contenido.
- **Garantía de devolución 7 días** sin preguntas — elimina la fricción de compra sin exponer el catálogo completo.
- **Sin acceso gratuito a la suscripción** — esa mecánica invita al abuso (descarga todo y cancela). La muestra F1 es un plan individual, no acceso temporal al catálogo completo.
- Botón CTA principal: cian (#29C0F5) con texto carbón. Rojo reservado para alertas únicamente.

---

## 10. Go to market

### Canal principal: contenido + comunidad

Las maestras de escuela privada son altamente activas en Instagram y grupos de WhatsApp del gremio. El canal de distribución más eficiente es el **word of mouth entre colegas** activado por la comunidad de la plataforma.

**Apalancamiento:**
1. Contenido orgánico en Instagram (reels de actividades, tips NEM, before/after de planes)
2. Grupos de Facebook y WhatsApp de maestras — distribución horizontal
3. Programa de afiliadas (25% recurrente año 1) — las más activas de la comunidad
4. Pauta Meta Ads como acelerador, no como canal principal

### Presupuesto de pauta y bumps

| Período | Presupuesto pauta | Trigger de bump |
|---|---|---|
| Jun–Ago 2026 | $5,000–$8,000/mes | CAC verano $130 |
| Sep–Nov 2026 | $30,000/mes | Ciclo escolar |
| Mes 18 | $50,000/mes | Bump automático al llegar a $250K/mes utilidad |
| Mes 23 | $70,000/mes | Siguiente bump |
| Mes 31 | $90,000/mes | Siguiente bump |
| Mes 34 | $110,000/mes | Siguiente bump |

**Regla de pauta:** si CAC > $300, pausar bump automático y optimizar copy/audiencia antes de escalar.

### CAC por período

| Período | CAC objetivo |
|---|---|
| Verano (Jun–Ago) | $130 MXN |
| Regreso a clases (Ago–Sep) | $150 MXN |
| Ciclo escolar normal | $200 MXN |

---

## 11. Modelo financiero — 36 meses

### Supuestos base

- **Churn:** 20% en verano (Meses 1–3), 12% en diciembre, 15% ciclo normal
- **Reactivación post-verano:** 65% (conservador — el modelo sigue siendo positivo con 50%)
- **LTV:** ($314 ARPU / 0.15 churn) × 0.93 tasa de retención = **$1,947 MXN**
- **LTV:CAC:** $1,947 / $200 = **9.7x** (CAC lanzamiento agosto $200 con pauta $20K) (mínimo viable es 3x)
- **Equilibrio** ($30K pauta, CAC $200) = 1,000 suscriptoras

### Costos operativos fijos mensuales

| Concepto | Costo/mes |
|---|---|
| Infra/Hosting propio (VPS + BD + CDN + SendGrid) | $1,200 MXN |
| Claude Max 20x (pipeline IA) | $3,900 MXN |
| Agencia ACMA (contenidos + redes) | $8,200 MXN |
| Foto + Actriz (sesión cada 2 meses) | $1,000 MXN (promedio) |
| SendGrid (email transaccional) | $0 (free tier) |
| GitHub Actions (automatización) | $0 (free tier) |
| **Total ops fijo** | **$14,300 MXN/mes** |

*Programador dev ($4,500/mes) solo durante Jun–Jul 2026 — costo único de setup del pipeline.*

### Inversión total

| Concepto | Monto |
|---|---|
| Infra/Hosting propio × 2 meses | $2,400 MXN |
| Claude Max 20x (API) × 2 meses | $7,800 MXN |
| Agencia ACMA × 2 meses | $16,400 MXN |
| Programador × 2 meses (Jun: plataforma · Jul: agentes) | $9,000 MXN |
| Foto + Actriz (sesión Jun) | $2,000 MXN |
| Dominio (año 1) | $300 MXN |
| **Subtotal pre-lanzamiento** | **$37,900 MXN** |
| Ops Jun–Jul sin ingresos (desarrollo) | $28,600 MXN |
| **Subtotal ops desarrollo** | **$28,600 MXN** |
| **INVERSIÓN TOTAL** | **$66,500 MXN** |


### Proyección mensual — primeros 16 meses

| M | Calendario | ARPU | Pauta | Nuevas | Subs | Ingresos | Resultado | Acumulado |
|---|---|---|---|---|---|---|---|---|
| 1 | Jun 2026 | — | — | — | 0 | $0 | -$14,300 | -$14,300 |
| 2 | Jul 2026 | — | — | — | 0 | $0 | -$14,300 | -$28,600 |
| 3 | **Ago 2026** | $297 | $20,000 | 100 | 100 | $29,700 | -$5,996 | -$34,596 |
| 4 | Sep 2026 | $297 | $30,000 | 150 | 235 | $69,795 | +$22,215 | -$12,381 |
| **5** | **Oct 2026 ✅** | $297 | $20,000 | 100 | 300 | $89,100 | +$50,612 | **+$38,231** |
| 6 | Nov 2026 | $297 | $10,000 | 60 | 315 | $93,555 | +$64,858 | +$103,089 |
| 7 | Dic 2026 | $297 | $5,000 | 30 | 307 | $91,179 | +$67,594 | +$170,683 |
| 8 | Ene 2027 | $297 | $15,000 | 80 | 341 | $101,277 | +$67,217 | +$237,900 |
| 12 | May 2027 | $297 | $15,000 | 80 | 448 | $133,056 | +$97,502 | +$589,132 |
| 13 | Jun 2027 | $314 | $5,000 | 20 | 378 | $118,692 | +$93,813 | +$682,946 |
| 15 | Ago 2027 | $357 | $30,000 | 200 | 474 | $169,218 | +$116,965 | +$876,967 |
| 16 | Sep 2027 | $357 | $30,000 | 180 | 583 | $208,131 | +$154,049 | +$1,031,015 |

> M1–M2 son desarrollo puro (Jun–Jul). M3 es el primer mes de operación real (Agosto). Ingresos = Subs × ARPU. Resultado = Ingresos – Ops $14,300 – Comisión Stripe ~4.7% – Pauta.

### Proyección de hitos — 36 meses

| Hito | Mes | Detalle |
|---|---|---|
| Lanzamiento | **M1 Ago 2026** | Ciclo escolar · Plan Solo/Plus/Escuela · Muestra gratis F1 · Pauta $30K |
| Inversión recuperada | **M5 Oct 2026** | $66,500 recuperados |
| $250K utilidad/mes | **M16 Ago 2027** | ARPU maduro $357, mix 30/55/15 |
| Primer bump de pauta | M18 | $30K → $50K |
| Segundo bump | M23 | $50K → $70K |
| Tercer bump | M31 | $70K → $90K |
| Cuarto bump | M34 | $90K → $110K |
| Utilidad M36 | M36 Jun 2029 | ~$929K/mes (lanzamiento Ago 2026 = M1) |
| **Acumulado 36 meses** | — | **$14,149,757 MXN** |
| **ROI** | — | **213x** |

### Cashflow Jun–Jul 2026 (desarrollo — sin ingresos)

| Concepto | Jun | Jul | Total |
|---|---|---|---|
| Ingresos (desarrollo puro — sin ventas) | $0 | $0 | $0 |
| Infra/hosting propio | -$1,200 | -$1,200 | -$2,400 |
| Claude Max 20x | -$3,900 | -$3,900 | -$7,800 |
| Programador dev | -$4,500 | -$4,500 | -$9,000 |
| Dominio | -$300 | — | -$300 |

| **Resultado operativo** | **-$14,300** | **-$14,300** | **-$28,600** |

---

## 12. Operación y stack tecnológico

### Plataforma de pagos y entrega

**pasarela integrada (Stripe/Conekta)** — seleccionado para el lanzamiento.

- Checkout y membresía en pasarela integrada (Stripe/Conekta) (checkout.clasemaestra.mx)
- Landing page externa (GitHub Pages) con diseño propio
- Los emails transaccionales usan de pasarela integrada (Stripe/Conekta) independientemente de la landing
- Breakeven vs plataforma fija: pasarela integrada (Stripe/Conekta) es más barato por debajo de ~$55,000–60,000 MXN/mes de revenue. Migración a stack propio post-validación de revenue. El sistema propio escala desde el día 1.

### Stack tecnológico completo

| Herramienta | Rol | Costo |
|---|---|---|
| Infra/hosting propio | Plataforma de membresía y entrega de contenido | $1,200/mes |
| Claude Max 20x (API) | Pipeline de generación de contenido | $3,900/mes |
| pasarela integrada (Stripe/Conekta) | Pagos y checkout | 7% por transacción |
| SendGrid | Email transaccional | $0 (free tier) |
| GitHub Actions | Automatización del pipeline mensual | $0 (free tier) |
| GitHub Pages | Hosting de landing y documentos | $0 |
| Make.com | Fallback de automatización si plataforma propia no tiene API | $0–$29/mes |

### Productos en plataforma propia (8 productos)

| Clave | Producto | Drip |
|---|---|---|
| solo_es | clasemaestra Solo — Español | Por inscripción |
| solo_en | clasemaestra Solo — English | Por inscripción |
| solo_bi | clasemaestra Solo — Bilingüe | Por inscripción |
| plus_es | clasemaestra Plus — Español | Por inscripción |
| plus_en | clasemaestra Plus — English | Por inscripción |
| plus_bi | clasemaestra Plus — Bilingüe | Por inscripción |
| bonos_es/en | Bonos Estacionales | Fecha calendario fija |
| comunidad | Comunidad Privada | Sin drip |

---

## 13. Pipeline de contenido — 5 agentes Claude

El sistema corre automáticamente el día 1 de cada mes vía GitHub Actions.

### Arquitectura de 5 agentes

```
Agente 0 (Métricas plataforma propia) ─┐
Agente 1 (Monitor SEP) ─────┤→ Briefing combinado + Reporte ejecutivo (email 8am)
                             ↓
                  Ventana de pausa 8am–10am
                             ↓
Agente 2 (Generador NEM) ← usa briefing de 0+1
                             ↓
Agente 3 (Revisor NEM) — score ≥85 aprueba — máx 2 iteraciones
                             ↓ aprobado
Agente 4 (Traductor) → ES + EN + Bilingüe
                             ↓
HTML render (Jinja2) → API propia → 3 versiones × N planes del mes
                             ↓
Confirmación email (6pm)
```

### Roles de cada agente

| Agente | Función | Output |
|---|---|---|
| Agente 0 | Lee métricas plataforma propia: vistas, tiempo de lectura, engagement por grado | Briefing para Agente 2 + Sección 1 del reporte ejecutivo |
| Agente 1 | Monitorea SEP, MEJOREDU, tendencias educativas (URLs fijas + web search libre) | Briefing curricular + Sección 2 del reporte ejecutivo |
| Agente 2 | Genera planes NEM completos (5 días × 45 min) usando el briefing de 0+1 | JSON con plan completo por grado y campo formativo |
| Agente 3 | Valida alineación NEM 2022. Score ≥85 = aprueba. Score <85 = rechaza con observaciones accionables | JSON con aprobado/rechazado + score + observaciones |
| Agente 4 | Traduce plan aprobado. Adaptación pedagógica, no traducción literal | 3 versiones: ES + EN + Bilingüe |

### Reporte ejecutivo mensual

Se envía a las 8am del día 1. Tiene 3 secciones:
1. **Métricas del negocio:** suscriptoras activas, nuevas, cancelaciones, churn, top 5 planes, proyección ingresos
2. **Monitor educativo:** cambios SEP, novedades NEM, impacto en contenido del mes
3. **Plan de contenido:** lista de planes a generar con fechas de publicación en plataforma propia

Ventana de pausa 8am–10am: si se crea `PAUSAR.flag` en el repo, el pipeline se detiene.

### Nomenclatura NEM 2022

El Agente 2 siempre usa terminología exacta NEM 2022:
- "Lenguajes" (nunca "Español")
- "Saberes Matemáticos" (nunca "Matemáticas")
- "Campo Formativo" + "Eje Articulador" + "Aprendizaje Esperado"

El Agente 4 adapta pedagógicamente para inglés:
- "Lenguajes" → "Language Arts" (nunca "Languages")
- "Saberes Matemáticos" → "Mathematics"
- "Campo Formativo" → "Learning Domain"

### Desarrollo del pipeline — cronograma

- **Inicio:** Lunes 1 de junio 2026
- **Fin:** Viernes 10 de julio 2026 (30 días hábiles, 6 semanas)
- **Stack:** Python 3.11 + anthropic SDK + API propia + SendGrid + GitHub Actions
- **Costo programador:** $4,500 MXN/mes × 2 = $9,000 MXN total

---

## 14. Roadmap

### Ciclo 1 — Arranque (Jun–Ago 2026)

- **Lanzamiento Agosto 2026** · Ciclo escolar · Plan Solo/Plus/Escuela · Muestra gratis F1
- Setup plataforma propia: 8 productos, drip configurado
- Sprint de producción: año escolar 2026–2027 completo
- Pipeline de 5 agentes en producción
- Ignición de comunidad: embajadoras + rituales + activación manual

### Ciclo 2 — Ciclo Escolar (Sep–Nov 2026)

- Escala ciclo escolar · primeras escuelas · Q&A en vivo inaugural
- Pauta $30K activa para regreso a clases
- Primeras escuelas (Plan Escuela $997)
- Breakeven: Mes 6 Noviembre

### Ciclo 3 — Escala (Dic 2026–Jun 2027)

- Mix Solo/Plus/Escuela maduro
- Validación precio inglés (encuesta Mes 6–8)
- Fase B del foso: editor en plataforma con tracking de edición
- Bump de pauta: $30K → $50K al llegar a $250K/mes de utilidad (Mes 16)

### Pendiente para próximas sesiones

- **Naming final** (clasemaestra está en uso, confirmar disponibilidad de marca)
- **Manual de identidad:** logo definitivo, paleta, tipografía, tono de voz
- **Landing page:** copy completo, estructura de conversión, CTA
- **Redes sociales:** estrategia de contenido orgánico, calendario editorial

---

## 15. Riesgos y mitigación

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| CAC supera $250 en escala | Media | Alto | Pauta cap + optimización copy antes de bump. LTV:CAC positivo hasta $300. |
| Reactivación post-verano < 80% | Media | Medio | Modelo usa 65%. Con 50% el negocio sigue positivo en septiembre. |
| Retención al cierre de ciclo | Media | Alto | Tres capas: contenido nuevo (SEP actualiza, maestras rotan grado) + lock-in de trabajo personalizado + pertenencia a comunidad. |
| Competencia de IA directa | Alta a 24 meses | Alto | Los tres fosos (data de outcome + lock-in de plataforma + comunidad) no se replican con un prompt. Ver sección 4. |
| Drip personal vs contenido estacional | Baja | Medio | Resuelto: drip = evergreen. Estacional = bonos por calendario. Dos canales independientes en plataforma propia. |
| Calidad cae con volumen | Media | Alto | Pipeline con revisor NEM (Agente 3, score ≥85 para publicar). Calidad sobre volumen. |
| plataforma propia sin API en plan Growth | Media | Medio | Fallback Make.com (mismo resultado, +3h de setup). Verificar el Día 1 del dev. |
| Comunidad no enciende | Alta sin ignición | Alto | 60–90 días de activación manual obligatoria. Si no hay persona dedicada, no prometer comunidad robusta al lanzar. |

---

## 16. Pendientes críticos antes de producción

### Urgente — hacer esta semana

- [ ] **Regenerar el PAT de GitHub** — el token quedó expuesto en conversación. GitHub → Settings → Developer settings → Personal access tokens → Revoke y generar nuevo.

### Antes de contratar al programador

- [ ] **Verificar API plataforma propia:** ir a plataforma propia → Settings → API y confirmar si el plan Growth tiene token disponible. Si no hay API, informar al programador antes de que cotice (el scope cambia).
- [ ] **Descargar PDFs NEM 2022** de `curriculobasica.sep.gob.mx` → Plan de Estudios 2022 + Programas de estudio por grado. Guardar en carpeta `docs/` para entregárselos al programador el Día 1.

### Antes del lanzamiento

- [ ] Definir naming final y verificar disponibilidad de marca
- [ ] Manual de identidad completo
- [ ] Landing page con copy de conversión
- [ ] Estrategia de contenido orgánico para redes
- [ ] Validación de precio $297 con primeras suscriptoras antes del ciclo escolar
- [ ] Configurar plataforma propia: crear los 8 productos (Solo/Plus × ES/EN/Bi + Bonos + Comunidad)
- [ ] Preparar API keys: CLAUDE_API_KEY, KAJABI_API_KEY, SENDGRID_API_KEY
- [ ] Encuesta a suscriptoras Mes 6–8 para validar precio inglés antes de campaña

---

## Referencias y documentación técnica

| Documento | URL |
|---|---|
| Business Case completo | https://quadrant-agency.github.io/propira/maestrolibrary/business-case.html |
| Dev Brief — arquitectura 5 agentes | https://quadrant-agency.github.io/propira/maestrolibrary/dev-brief.html |
| Manual técnico del programador | https://quadrant-agency.github.io/propira/maestrolibrary/manual.html |
| Gantt 6 semanas | https://quadrant-agency.github.io/propira/maestrolibrary/gantt.html |
| Repositorio GitHub | https://github.com/quadrant-agency/propira |

---

*clasemaestra · Confidencial · Junio 2026 · Quadrant Agency*
