# Propuesta de Diseño: Cova Hedin — Premium

## Identidad
Cova Hedin es una educadora de sueco de 25 años nacida en Gotemburgo, Suecia, hija de madre sueca y padre latinoamericano, actualmente viviendo en Italia. Encarna la fusión de minimalismo escandinavo y calidez latina — "A Swedish Latina in Italy". Con 10K+ clases, 5,312 reviews perfectas, y 39K seguidores en Instagram, no es solo una profesora: es una marca educativa consolidada que hace el sueco visual, divertido y accesible.

## Audiencia
1. **Estudiantes potenciales** de sueco (todos los niveles) → necesitan ver credenciales, reviews, y un CTA de booking claro
2. **Empresas/plataformas** buscando colaboración → "Work with me" visible, track record con StoryLearning y Language Lock-In
3. **Seguidores de redes** (IG/TikTok/YouTube) → hub central, proof de expertise, enlaces a plataformas

## Secciones Propuestas (en orden)

### 1. Header — Floating Pill Nav
Nav links: About · Languages · Reviews · Services · Content · Contact
Aparece como pill glassmorphism al hacer scroll >400px

### 2. Hero — "Hej! I'm Cova"
```
MOBILE (375px):
┌─────────────────────┐
│    [Foto circular]   │
│                       │
│    Cova Hedin        │
│    Swedish Teacher    │
│    & Content Creator  │
│                       │
│  "Ready to learn     │
│   Swedish?"          │
│                       │
│  [🇸🇪 Book a Lesson] │
│  [💼 Work with Me]   │
│                       │
│  ┌──┬──┬──┬──┐       │
│  │IG│TT│YT│LI│       │
│  └──┴──┴──┴──┘       │
│                       │
│ ┌─────┬─────┬─────┐  │
│ │500+ │10K+ │ 7+  │  │
│ │stud.│less.│years│  │
│ └─────┴─────┴─────┘  │
└───────────────────────┘

DESKTOP:
┌──────────────────────────────────────────┐
│  [Foto cuadrada    │  Cova Hedin         │
│   rounded-2xl      │  Swedish Teacher &  │
│   con borde        │  Content Creator    │
│   accent]          │                     │
│                    │  "Ready to learn    │
│                    │   Swedish?"         │
│                    │                     │
│                    │  [Book] [Work w/Me] │
│                    │  [IG][TT][YT][LI]  │
│─────────────────────────────────────────│
│  500+ students  │  10K+ lessons  │  7+ yrs │
└──────────────────────────────────────────┘
```
- Emojis OK (ella pidió)
- Stats bar con números grandes en accent color
- Dual CTA: booking (primary) + collab (secondary outline)

### 3. About — "A Swedish Latina in Italy"
```
MOBILE:
┌───────────────────────┐
│  About Me              │
│  ─────────             │
│                        │
│  [Texto bio de su CV,  │
│   3 párrafos]          │
│                        │
│  ┌────────────────┐    │
│  │ "Learning      │    │
│  │  Swedish should│    │
│  │  be effective, │    │
│  │  structured,   │    │
│  │  and enjoyable"│    │
│  └────────────────┘    │
└────────────────────────┘

DESKTOP:
┌──────────────────────────────────────────┐
│  About Me             │  ┌────────────┐  │
│  ─────                │  │ Pull quote │  │
│  [Bio text            │  │ "Learning  │  │
│   3 párrafos          │  │  Swedish..." │
│   usando sus textos]  │  └────────────┘  │
└──────────────────────────────────────────┘
```

### 4. Languages I Speak — SECCIÓN ÚNICA ⭐
Efecto visual único: 6 idiomas como tarjetas con bandera/emoji + nombre
```
MOBILE (2 cols):
┌──────────┬──────────┐
│ 🇸🇪 Swedish│ 🇬🇧 English│
├──────────┼──────────┤
│ 🇪🇸 Spanish│ 🇮🇹 Italian│
├──────────┼──────────┤
│ 🇮🇱 Hebrew │ 🇵🇪 Quechua│
└──────────┴──────────┘

DESKTOP (6 cols, una fila):
┌────┬────┬────┬────┬────┬────┐
│ 🇸🇪  │ 🇬🇧  │ 🇪🇸  │ 🇮🇹  │ 🇮🇱  │ 🇵🇪  │
│Swe │Eng │Spa │Ita │Heb │Que │
└────┴────┴────┴────┴────┴────┘
```
Cards con hover scale + accent border. Efecto reveal stagger.
Ella específicamente pidió esto como su sección "Specialties" à la Annie.

### 5. My Approach — "What Makes My Lessons Special"
```
MOBILE:
┌────────────────────────┐
│  What Makes My Lessons │
│  Special               │
│                        │
│  ✔ Visual & engaging   │
│    materials           │
│  ✔ Structured sessions │
│  ✔ Conversation-focused│
│  ✔ Clear milestones    │
│  ⭐ Free materials +   │  ← highlighted!
│     homework included  │
│                        │
│  [CTA: Book a lesson]  │
└────────────────────────┘
```
Último item ("Free materials + homework") con highlight especial (background accent, icono, o badge "Included") como ella pidió.

### 6. Testimonials — "What My Students Say" ⭐⭐
SECCIÓN MÁS PROMINENTE. Ella pidió foco aquí.
3 reviews de italki (pinned ones). Cards grandes con nombre, país, texto.
```
MOBILE:
┌────────────────────────┐
│  What My Students Say  │
│  5,312 reviews · ⭐⭐⭐⭐⭐│
│                        │
│  ┌──────────────────┐  │
│  │ "Cova is a very  │  │
│  │  understanding   │  │
│  │  teacher..."     │  │
│  │  — Julia, Russia │  │
│  └──────────────────┘  │
│                        │
│  ┌──────────────────┐  │
│  │ "I've improved   │  │
│  │  tremendously..." │ │
│  │  — Student, intl  │  │
│  └──────────────────┘  │
│                        │
│  ┌──────────────────┐  │
│  │ "Enthusiastic    │  │
│  │  about teaching" │  │
│  │  — Student       │  │
│  └──────────────────┘  │
│                        │
│  [See all on italki →] │
└────────────────────────┘

DESKTOP (3-col grid):
┌─────────┬─────────┬─────────┐
│ Review 1│ Review 2│ Review 3│
│ —Julia  │ —Name   │ —Name   │
└─────────┴─────────┴─────────┘
```
Badge "5,312 reviews · 5/5 ⭐" en header de sección.

### 7. Experience — Collaborations & Track Record
Timeline horizontal con 3 entries:
```
──●──────────●──────────●──
  italki    Language   Story
  10K+      Lock-In    Learning
  lessons   Head       Course
            Teacher    Creator
```
NO mostrar como "proyectos/competidores" (ella lo dudó).
Mostrar como **credenciales** — donde ha enseñado/creado cursos.

### 8. Services — What I Offer
Grid de 3-4 cards:
- 🎓 Private Lessons (1:1, all levels A0→C1+)
- 👥 Group Lessons (max 3 students)
- 🏢 Corporate Training (custom Swedish programs)
- 🌐 Translation & Proofreading

Cada card con breve descripción + CTA "Learn more" → SimplyBook

### 9. Latest Content — "From My Channels"
En lugar de "Latest Articles" (como ella pidió):
3 thumbnail cards que linkean a sus últimos reels/videos.
Implementar como cards estáticas con imagen + título + link a IG/YouTube.

### 10. CTA — "Ready to Start Learning Swedish?"
Full-width section con background accent suave.
Dual CTA: [Book a Lesson] + [Work with Me]
Email: swedishwithcova@gmail.com

### 11. Footer
Social icons (IG, TikTok, YT, LinkedIn) + email + copyright
Background primaryDark (azul oscuro sueco)

## Secciones que NO incluir
- **Education formal** — No tiene grado universitario público; su credibilidad viene de experiencia (10K+ lessons, reviews)
- **Skills pills genéricas** — No aplica, sus "skills" son los idiomas (ya cubiertos en Languages)
- **Blog** — No tiene blog; reemplazado por "Latest Content" (reels/videos)
- **Projects grid genérico** — No aplica; sus "proyectos" son competidores (StoryLearning, Language Lock-In) y van como Experience/credenciales

## Metáfora Visual
El minimalismo claro y funcional de un día de verano en Estocolmo — cielo celeste, sol amarillo dorado reflejando en el agua — combinado con la calidez y energía de su identidad latina. Un portfolio que se siente como una clase con Cova: limpio, visual, acogedor, y eficiente.

## Paleta (6 colores)

| Token | Color | Justificación |
|-------|-------|---------------|
| primaryDark | `#0f2b4c` | Azul profundo sueco — autoridad, encabezados, footer bg |
| primary | `#1d5a8c` | Azul sueco medio — bordes, nav, badges |
| primaryLight | `#7ab8d9` | Celeste sueco — shimmer highlights, acentos suaves |
| accent | `#f0c75e` | Amarillo sueco dorado pastel — CTAs, stats, bullet dots, el color que POP |
| surface | `#faf8f5` | Off-white cálido — backgrounds de secciones (como slowswedish.com) |
| surfaceLight | `#ffffff` | Blanco puro — hero bg, secciones alternadas |

## Tipografía
- **Headlines:** DM Serif Display — elegante, autoritaria, similar a Kudryashev de slowswedish.com
- **Body:** Plus Jakarta Sans — moderna, friendly, legible
- **Accent/stats:** Space Mono — monospace para stats/badges (como slowswedish.com labels)

## Efecto Visual Único
**Language cards con flags** — sección de idiomas con 6 tarjetas que muestran emoji de bandera + idioma, con hover scale + accent border glow. En scroll, aparecen con stagger reveal. Ningún otro portfolio nuestro tiene esta visualización.
