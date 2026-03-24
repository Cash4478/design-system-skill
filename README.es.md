# Generador de Design System — Claude Code Skill

### Genera design.md, design-guidelines.md y design-components.md desde cualquier referencia de diseno

**[🇨🇳 中文](README.zh-CN.md)** | **🇪🇸 Espanol** | **[🇺🇸 English](README.md)**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/Skill-blue?style=flat-square" alt="Skill">
  <img src="https://img.shields.io/github/license/albertzhangz10/design-system-skill?style=flat-square&color=green" alt="MIT License">
  <img src="https://img.shields.io/github/stars/albertzhangz10/design-system-skill?style=flat-square" alt="GitHub Stars">
</p>

> Deja de documentar tu design system manualmente. Sube cualquier referencia de diseno y obtiene 3 archivos Markdown listos para produccion que las herramientas de programacion con IA (Cursor, Claude Code, Copilot) entienden nativamente.

**[O usa la version web — sin instalacion](https://figmadesignmd.com/)**

Un skill de Claude Code que genera documentacion completa de design systems a partir de cualquier material de referencia: imagenes, PDFs, enlaces, capturas de pantalla, guias de marca o codigo existente. Los usuarios no tecnicos (disenadores, PMs) pueden usar la [version web](https://figmadesignmd.com/) directamente.

## El Problema

Los design systems viven en Figma, PDFs de marca y documentos dispersos, pero la documentacion que las herramientas de IA necesitan no existe. Cada vez que inicias un proyecto nuevo, escribes manualmente las especificaciones de tokens, guias de componentes y reglas de accesibilidad.

## La Solucion

Un comando. Tres documentos. Desde cualquier referencia de diseno.

```
/design-system
```

## Que Genera

| Archivo | Contenido | Auto |
|---------|-----------|:----:|
| **design.md** — colores, tipografia, forma, elevacion, estados, layout, movimiento | Archivos de tokens, imagenes, PDFs | ✅ |
| **design-guidelines.md** — accesibilidad, gestos, diseno de contenido, buenas y malas practicas | Referencias + inferencia | ✅ |
| **design-components.md** — 30+ componentes con variantes, medidas, estados | Referencias + inferencia | ✅ |

## Como Funciona

```
Paso 1  Proporciona cualquier referencia de diseno (imagenes, PDFs, enlaces, texto, codigo)
Paso 2  La IA analiza el lenguaje de diseno en todos los materiales
Paso 3  Genera 3 archivos Markdown estructurados
Paso 4  Escribe los archivos en el directorio del proyecto
Paso 5  Confirma con el usuario antes de guardar
```

### Entradas Aceptadas

| Tipo | Ejemplos |
|------|----------|
| Imagenes | Capturas de pantalla, mockups, exportaciones de herramientas de diseno |
| PDFs | Guias de marca, guias de estilo, especificaciones de diseno |
| Enlaces | Documentacion de design systems, bibliotecas de componentes, sitios web en vivo |
| Texto | Descripciones escritas del lenguaje de diseno |
| Codigo | Archivos CSS, configuraciones de Tailwind, archivos de tema, tokens de diseno |

### Formato de Salida

Cada archivo:
- Comienza con un titulo H1 y referencias cruzadas a los otros 2 archivos
- Usa tablas Markdown para valores de tokens y especificaciones de componentes
- Incluye medidas especificas (dp/sp/px), colores hexadecimales y valores CSS
- Organiza buenas y malas practicas por categoria (Color, Forma, Elevacion, Tipografia, etc.)
- Agrupa componentes por flujo de trabajo (Acciones, Entrada, Navegacion, Contenedores, Retroalimentacion)

### Cobertura de Componentes

| Categoria | Componentes |
|-----------|------------|
| **Acciones** | Button, Icon Button, FAB, Toolbar, Link |
| **Entrada** | Text Field, Checkbox, Radio, Switch, Slider, Dropdown, Combobox, Picker, Textarea |
| **Navegacion** | Nav Bar/Rail/Drawer, Tabs, Breadcrumb, Menu, Search, App Bar |
| **Contenedores** | Card, Dialog, Bottom Sheet, Drawer, Popover, Accordion, Divider |
| **Visualizacion de Datos** | Avatar, Badge, List, Carousel, Icon, Image, Tag/Chip, Skeleton, Tooltip |
| **Retroalimentacion** | Progress Indicator, Spinner, Snackbar/Toast, Message Bar |

## Instalacion

```bash
# Clona en tu directorio .claude/skills
git clone https://github.com/albertzhangz10/design-system-skill.git .claude/skills/design-system
```

O copia el archivo `SKILL.md` en el directorio `.claude/skills/design-system/` de tu proyecto.

## Uso

```
/design-system                    # genera en el directorio actual
/design-system ./docs/            # ruta de salida personalizada
```

Luego proporciona tus referencias de diseno: arrastra y suelta imagenes, pega enlaces o describe el lenguaje de diseno.

## Requisitos

| Requisito | Requerido | Notas |
|-----------|:---------:|-------|
| Claude Code | ✅ | Se recomienda la ultima version |
| Referencias de diseno | ✅ | Cualquier combinacion de imagenes, PDFs, enlaces, texto o codigo |

## Licencia

Licencia MIT — consulta el archivo [LICENSE](LICENSE) para mas detalles.

## Creditos

Creado por [Albert Zhang](https://github.com/albertzhangz10).

Inspirado en [Google Stitch design.md](https://stitch.withgoogle.com/docs/design-md/overview) — el formato y la estructura de `design.md` se basan en su trabajo.
