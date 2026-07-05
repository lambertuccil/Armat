# Paleta de Colores — ARMAT

## Colores Primarios

### Negro
```css
--color-negro: #000000;
--color-negro-rgb: 0, 0, 0;
```
**Uso**: Fondo principal, texto en claro
**Aplicaciones**: Fondos de sección, headers, footer

### Dorado
```css
--color-dorado: #C9A96E;
--color-dorado-rgb: 201, 169, 110;
```
**Uso**: Acentos, badges, highlights
**Aplicaciones**: Títulos destacados, badges, botones, bordes decorativos

### Blanco
```css
--color-blanco: #FFFFFF;
--color-blanco-rgb: 255, 255, 255;
```
**Uso**: Texto en oscuro, fondos
**Aplicaciones**: Texto sobre negro, fondos limpios

## Colores Secundarios

### Gris Oscuro
```css
--color-gris-oscuro: #1A1A1A;
```
**Uso**: Texto principal
**Aplicaciones**: Títulos, texto cuerpo importante

### Gris
```css
--color-gris: #666666;
```
**Uso**: Texto secundario
**Aplicaciones**: Descripciones, texto cuerpo

### Gris Claro
```css
--color-gris-claro: #999999;
```
**Uso**: Metadata, labels
**Aplicaciones**: Fechas, categorías, labels pequeños

### Borde
```css
--color-borde: #E8E8E8;
```
**Uso**: Divisores, bordes
**Aplicaciones**: Líneas separadoras, bordes de cards

### Background
```css
--color-background: #F5F5F5;
```
**Uso**: Cards, fondos suaves
**Aplicaciones**: Fondos de secciones alternas, cards

### Page Background
```css
--color-page-bg: #E5E5E5;
```
**Uso**: Fondo de pantalla
**Aplicaciones**: Fondo general de la página

## Combinaciones Aprobadas

### Sobre Fondo Negro
| Texto | Contraste | Uso |
|-------|-----------|-----|
| Blanco #FFFFFF | 21:1 | Texto principal |
| Dorado #C9A96E | 8.5:1 | Acentos |
| Gris claro #999999 | 4.5:1 | Metadata |

### Sobre Fondo Blanco
| Texto | Contraste | Uso |
|-------|-----------|-----|
| Negro #000000 | 21:1 | Texto principal |
| Gris oscuro #1A1A1A | 18.5:1 | Texto cuerpo |
| Gris #666666 | 5.7:1 | Texto secundario |
| Dorado #C9A96E | 2.3:1 | Solo para badges grandes |

### Sobre Fondo Dorado
| Texto | Contraste | Uso |
|-------|-----------|-----|
| Negro #000000 | 8.5:1 | Texto principal |
| Blanco #FFFFFF | 2.3:1 | Solo para texto grande |

## Uso en CSS

### Variables
```css
:root {
  --color-negro: #000000;
  --color-dorado: #C9A96E;
  --color-blanco: #FFFFFF;
  --color-gris-oscuro: #1A1A1A;
  --color-gris: #666666;
  --color-gris-claro: #999999;
  --color-borde: #E8E8E8;
  --color-background: #F5F5F5;
  --color-page-bg: #E5E5E5;
}
```

### Ejemplos de Uso
```css
/* Fondo negro con texto blanco */
.header {
  background: var(--color-negro);
  color: var(--color-blanco);
}

/* Acento dorado */
.badge {
  background: var(--color-dorado);
  color: var(--color-negro);
}

/* Texto secundario */
.metadata {
  color: var(--color-gris-claro);
  font-size: 12px;
}

/* Borde sutil */
.card {
  border: 1px solid var(--color-borde);
}
```

## Accesibilidad

### Contraste Mínimo
- **Texto normal**: 4.5:1 (WCAG AA)
- **Texto grande**: 3:1 (WCAG AA)
- **UI components**: 3:1 (WCAG AA)

### Verificación
Usar herramientas como:
- WebAIM Contrast Checker
- Chrome DevTools
- Colour Contrast Analyser

## Archivos de Color

### Para Diseñadores
- `ARMAT_palette.ase` (Adobe Swatch Exchange)
- `ARMAT_palette.sketchpalette` (Sketch)

### Para Desarrolladores
- `variables.css` (CSS custom properties)
- `tailwind.config.js` (Tailwind CSS)
- `scss/_variables.scss` (SCSS)