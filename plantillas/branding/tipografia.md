# TIPOGRAFÍA

> **NOTA:** Completar con las tipografías que el usuario elija. Definir tipografías para web, documentos legales y redes sociales. Incluir tamaños, pesos y uso de cada una.

---

## TIPOGRAFÍA PRINCIPAL

La tipografía principal es la que representa la identidad visual del estudio.

| Propiedad | Valor |
|-----------|-------|
| **Nombre** | [NOMBRE_TIPOGRAFIA_PRINCIPAL] |
| **Familia** | [FAMILIA: Serif / Sans-serif / Slab] |
| **Fuente** | Google Fonts / Adobe Fonts / Local |
| **URL** | [URL_FUENTE] |

### Ejemplo para estudio jurídico:

| Propiedad | Valor |
|-----------|-------|
| **Nombre** | Playfair Display |
| **Familia** | Serif |
| **Fuente** | Google Fonts |
| **URL** | https://fonts.google.com/specimen/Playfair+Display |

**¿Por qué serif?** Las tipografías serif transmiten tradición, seriedad y profesionalismo — cualidades deseables para un estudio jurídico.

---

## TIPOGRAFÍA SECUNDARIA

La tipografía secundaria complementa a la principal y se usa para textos largos y cuerpo de contenido.

| Propiedad | Valor |
|-----------|-------|
| **Nombre** | [NOMBRE_TIPOGRAFIA_SECUNDARIA] |
| **Familia** | [FAMILIA: Serif / Sans-serif / Slab] |
| **Fuente** | Google Fonts / Adobe Fonts / Local |
| **URL** | [URL_FUENTE] |

### Ejemplo:

| Propiedad | Valor |
|-----------|-------|
| **Nombre** | Inter |
| **Familia** | Sans-serif |
| **Fuente** | Google Fonts |
| **URL** | https://fonts.google.com/specimen/Inter |

**¿Por qué sans-serif para el cuerpo?** Las tipografías sans-serif son más legibles en pantallas y en textos largos, especialmente en dispositivos móviles.

---

## TIPOGRAFÍA MONOESPACIADA (OPCIONAL)

Para código, números de expediente o datos técnicos.

| Propiedad | Valor |
|-----------|-------|
| **Nombre** | [NOMBRE_TIPOGRAFIA_MONO] |
| **Familia** | Monospace |
| **Fuente** | Google Fonts / Local |
| **URL** | [URL_FUENTE] |

### Ejemplo:

| Propiedad | Valor |
|-----------|-------|
| **Nombre** | JetBrains Mono |
| **Familia** | Monospace |
| **Fuente** | Google Fonts |

---

## ESCALA DE TIPOGRAFÍA

### Para web:

| Elemento | Tamaño | Peso | Tipografía | Uso |
|----------|--------|------|------------|-----|
| H1 | [TAMAÑO_H1: 32-48px] | Bold / 700 | Principal | Títulos principales de página |
| H2 | [TAMAÑO_H2: 24-32px] | Semi-bold / 600 | Principal | Subtítulos de sección |
| H3 | [TAMAÑO_H3: 20-24px] | Medium / 500 | Principal | Subtítulos menores |
| H4 | [TAMAÑO_H4: 18-20px] | Medium / 500 | Secundaria | Encabezados de contenido |
| Body | [TAMAÑO_BODY: 16-18px] | Regular / 400 | Secundaria | Texto principal |
| Small | [TAMAÑO_SMALL: 14px] | Regular / 400 | Secundaria | Notas, pies de foto |
| Caption | [TAMAÑO_CAPTION: 12px] | Regular / 400 | Secundaria | Leyendas, metadatos |

### Para documentos legales:

| Elemento | Tamaño | Peso | Tipografía | Uso |
|----------|--------|------|------------|-----|
| Título del documento | 16pt | Bold | Serif | Títulos de demandas, contratos |
| Subtítulo | 14pt | Semi-bold | Serif | Secciones del documento |
| Cuerpo del texto | 12pt | Regular | Serif | Texto principal del escrito |
| Notas al pie | 10pt | Regular | Serif | Notas aclaratorias |
| Encabezado | 10pt | Bold | Sans-serif | Datos del expediente |

### Para redes sociales:

| Elemento | Tamaño | Peso | Tipografía |
|----------|--------|------|------------|
| Texto principal | 16-18px | Regular | Sans-serif |
| Título | 24-32px | Bold | Sans-serif o Serif |
| Call to action | 18-20px | Semi-bold | Sans-serif |

---

## PAIRING DE TIPOGRAFÍAS

### Combinación recomendada 1: Tradición y Legibilidad

| Uso | Tipografía | Razón |
|-----|-----------|-------|
| Títulos | Playfair Display (Serif) | Transmite elegancia y tradición |
| Cuerpo | Inter (Sans-serif) | Alta legibilidad en pantalla |

### Combinación recomendada 2: Modernidad y Profesionalismo

| Uso | Tipografía | Razón |
|-----|-----------|-------|
| Títulos | DM Serif Display (Serif) | Serif moderna y limpia |
| Cuerpo | DM Sans (Sans-serif) | Complementa perfectamente la serif |

### Combinación recomendada 3: Solidez y Claridad

| Uso | Tipografía | Razón |
|-----|-----------|-------|
| Títulos | Libre Baskerville (Serif) | Clásica y confiable |
| Cuerpo | Source Sans Pro (Sans-serif) | Legible y profesional |

---

## ESPECIFICACIONES PARA CSS

```css
/* Tipografía principal (títulos) */
--font-primary: '[NOMBRE_TIPOGRAFIA_PRINCIPAL]', serif;

/* Tipografía secundaria (cuerpo) */
--font-secondary: '[NOMBRE_TIPOGRAFIA_SECUNDARIA]', sans-serif;

/* Tipografía monoespaciada */
--font-mono: '[NOMBRE_TIPOGRAFIA_MONO]', monospace;

/* Tamaños */
--text-xs: 0.75rem;    /* 12px */
--text-sm: 0.875rem;   /* 14px */
--text-base: 1rem;     /* 16px */
--text-lg: 1.125rem;   /* 18px */
--text-xl: 1.25rem;    /* 20px */
--text-2xl: 1.5rem;    /* 24px */
--text-3xl: 1.875rem;  /* 30px */
--text-4xl: 2.25rem;   /* 36px */

/* Pesos */
--font-light: 300;
--font-regular: 400;
--font-medium: 500;
--font-semibold: 600;
--font-bold: 700;
```

---

## ESPECIFICACIONES PARA IMPRESIÓN

Para documentos legales impresos:

| Propiedad | Valor |
|-----------|-------|
| **Tamaño de letra base** | 12pt |
| **Interlineado** | 1.5 o 2.0 |
| **Márgenes** | [MARGEN_IZQUIERDO] x [MARGEN_DERECHO] x [MARGEN_SUPERIOR] x [MARGEN_INFERIOR] |
| ** Sangría** | 1.27 cm (1/2 pulgada) |
| **Alineación** | Justificado |

---

## REGLAS DE USO

1. **Consistencia:** Usar las mismas tipografías en todos los canales.
2. **Jerarquía:** Mantener una jerarquía clara entre títulos, subtítulos y cuerpo.
3. **Legibilidad:** Priorizar la legibilidad sobre la estética.
4. **Tamaños mínimos:** No usar tamaños menores a 12px en web ni 10pt en impresión.
5. **Pesos:** No usar más de 3 pesos diferentes por tipografía.
6. **Espaciado:** Mantener un interlineado de al menos 1.5 para cuerpo de texto.
7. **Negritas:** Usar negritas con moderación para resaltar palabras clave.

---

## CHECKLIST DE APLICACIÓN

- [ ] Las tipografías se cargan correctamente en el sitio web
- [ ] Los tamaños son legibles en dispositivos móviles
- [ ] La jerarquía tipográfica es clara
- [ ] Los documentos legales usan la tipografía correcta
- [ ] Las redes sociales mantienen la consistencia tipográfica
- [ ] Los pesos de fuente son consistentes
