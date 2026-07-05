# Ejemplos Marketing — ConstructoraAI

## Ejemplo 1: Brochure HTML Completo

### Input del Usuario:
"Creame el brochure de ENTANYQ para enviar por WhatsApp"

### Análisis:
- **Formato**: Brochure HTML
- **Plataforma**: WhatsApp (750px)
- **Propiedad**: ENTANYQ
- **Objetivo**: Vender departamentos

### Output:
```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ENTANYQ — ARMAT</title>
    <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'DM Sans', sans-serif; background: #E5E5E5; }
        .page { width: 750px; margin: 0 auto; background: #fff; }
        /* ... más estilos ... */
    </style>
</head>
<body>
    <!-- PORTADA -->
    <div class="page cover">
        <img src="img/render/AM.jpeg" alt="ENTANYQ">
        <div class="cover-info">
            <div class="logo">ARMAT</div>
            <h1>ENTANYQ</h1>
            <p>Departamentos en Centenario, Neuquén</p>
            <div class="specs">
                <span>34,5 – 45,5 m²</span>
                <span>Desde USD 60.000</span>
                <span>USD 1.739 – 1.868/m²</span>
            </div>
        </div>
        <div class="disclaimer">
            Renders ilustrativos. Acabados finales según memoria descriptiva.
        </div>
    </div>
    
    <!-- MÁS PÁGINAS... -->
</body>
</html>
```

### Características:
- Single-file (CSS inline)
- Google Fonts CDN
- Optimizado 750px WhatsApp
- Disclaimer incluido
- Paleta ARMAT (negro + dorado)

---

## Ejemplo 2: Flyer Instagram

### Input del Usuario:
"Post para Instagram mostrando nuevo avance de obra"

### Análisis:
- **Formato**: Flyer 1080x1080
- **Plataforma**: Instagram
- **Contenido**: Avance de obra
- **Estilo**: Informativo + premium

### Output:
```
# Flyer Instagram — Avance de Obra

## Diseño
- **Fondo**: Foto real de obra (obragris1.jpg)
- **Overlay**: Negro 60% opaco
- **Texto superior**: "AVANCE DE OBRA"
- **Texto central**: "50%"
- **Texto inferior**: "Mampostería completa"
- **CTA**: "Próximamente: Instalaciones interiores"
- **Badge**: "ENTANYQ — Centenario"
- **Footer**: Logo ARMAT + contacto

## Copy
🏗️ Obra al 50%

Mampostería completa. Próximamente: instalaciones interiores.

📍 Centenario, Neuquén
📞 299 508 9366
💰 Desde USD 60.000

#ARMAT #ENTANYQ #Centenario #ObraGris #Departamentos
```

---

## Ejemplo 3: Email de Seguimiento

### Input del Usuario:
"Email para un cliente que visitó la obra pero no cerró"

### Análisis:
- **Formato**: Email HTML
- **Objetivo**: Re-enganchar al cliente
- **Tono**: Cercano, profesional
- **CTA**: Coordinar segunda visita

### Output:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body style="font-family: 'DM Sans', sans-serif; max-width: 600px; margin: 0 auto;">
    
    <!-- Header -->
    <div style="background: #000; padding: 20px; text-align: center;">
        <h1 style="color: #C9A96E; font-family: 'Playfair Display', serif;">ARMAT</h1>
    </div>
    
    <!-- Contenido -->
    <div style="padding: 30px;">
        <h2 style="color: #000;">Hola [Nombre],</h2>
        
        <p style="color: #666; line-height: 1.8;">
            Te escribo para hacer seguimiento de tu visita a ENTANYQ.
        </p>
        
        <p style="color: #666; line-height: 1.8;">
            ¿Qué te pareció? ¿Tenés alguna consulta?
        </p>
        
        <div style="text-align: center; margin: 30px 0;">
            <a href="tel:2995089366" style="background: #C9A96E; color: #000; padding: 15px 30px; text-decoration: none; font-weight: 600;">
                LLAMANOS
            </a>
        </div>
        
        <p style="color: #666; line-height: 1.8;">
            Saludos,<br>
            <strong>ARMAT Desarrolladora Inmobiliaria</strong>
        </p>
    </div>
    
    <!-- Footer -->
    <div style="background: #F5F5F5; padding: 20px; text-align: center; font-size: 12px; color: #999;">
        299 508 9366 | @armat.desarrollos
    </div>
    
</body>
</html>
```

---

## Ejemplo 4: Post de Instagram (Copy)

### Input del Usuario:
"Copy para Instagram mostrando el departamento de 1 dormitorio"

### Análisis:
- **Formato**: Copy para post
- **Plataforma**: Instagram
- **Contenido**: Departamento 1 dormitorio
- **Estilo**: Venta + lifestyle

### Output:
```
# Copy Instagram — 1 Dormitorio

## Opción 1 (Enfocada en espacio)
🏠 Departamento de 1 dormitorio

45,5 m² de diseño moderno y funcional.
Balcón con vista.
Cochera disponible.

📍 Centenario, Neuquén
💰 Desde USD 85.000 (USD 1.868/m²)
📞 299 508 9366

#ARMAT #ENTANYQ #Centenario #Departamentos #1Dormitorio

---

## Opción 2 (Enfocada en inversión)
📈 Invertí en Centenario

Departamento de 1 dormitorio:
✅ 45,5 m²
✅ USD 85.000
✅ Zona en crecimiento (Vaca Muerta)
✅ 50% ya vendido

¿Querés saber más?
📞 299 508 9366

#ARMAT #ENTANYQ #Inversión #Centenario #VacaMuerta

---

## Opción 3 (Enfocada en estilo de vida)
✨ Viví como merecés

Departamento de 1 dormitorio en ENTANYQ:
• Diseño moderno
• Balcón privado
• Cocheras disponibles
• Zona premium

📍 Centenario, Neuquén
💰 Desde USD 85.000

#ARMAT #ENTANYQ #VidaModerna #Centenario
```

---

## Ejemplo 5: Brochure Comparativo

### Input del Usuario:
"Brochure comparando el monoambiente vs 1 dormitorio"

### Análisis:
- **Formato**: Brochure HTML
- **Contenido**: Comparativa
- **Objetivo**: Ayudar al cliente a decidir

### Output:
```html
<!-- PÁGINA COMPARATIVA -->
<div class="page">
    <h2>Comparativa ENTANYQ</h2>
    
    <div class="comparison">
        <div class="unit">
            <h3>Monoambiente</h3>
            <div class="price">USD 60.000</div>
            <div class="m2">34,5 m² (USD 1.739/m²)</div>
            <ul>
                <li>Compacto y funcional</li>
                <li>Ideal para inversores</li>
                <li>Menor inversión inicial</li>
            </ul>
        </div>
        
        <div class="vs">VS</div>
        
        <div class="unit">
            <h3>1 Dormitorio</h3>
            <div class="price">USD 85.000</div>
            <div class="m2">45,5 m² (USD 1.868/m²)</div>
            <ul>
                <li>Dormitorio separado</li>
                <li>Más espacio (32%)</li>
                <li>Ideal para vivir</li>
            </ul>
        </div>
    </div>
    
    <div class="cta">
        ¿Querés saber cuál es mejor para vos?
        <br>
        <strong>299 508 9366</strong>
    </div>
</div>
```

---

## Ejemplo 6: Plantilla de Email Marketing

### Input del Usuario:
"Template de email para nuevos leads"

### Análisis:
- **Formato**: Email HTML template
- **Objetivo**: Bienvenida a nuevos leads
- **Tono**: Profesional, cercano

### Output:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body style="font-family: 'DM Sans', sans-serif; max-width: 600px; margin: 0 auto; background: #ffffff;">
    
    <!-- Header -->
    <div style="background: #000000; padding: 30px; text-align: center;">
        <h1 style="color: #C9A96E; font-family: 'Playfair Display', serif; margin: 0;">ARMAT</h1>
        <p style="color: rgba(255,255,255,0.6); margin: 5px 0 0 0; font-size: 12px;">Desarrolladora Inmobiliaria</p>
    </div>
    
    <!-- Contenido Principal -->
    <div style="padding: 40px 30px;">
        <h2 style="color: #000000; font-family: 'Playfair Display', serif;">¡Bienvenido!</h2>
        
        <p style="color: #666666; line-height: 1.8;">
            Gracias por interesarte en nuestros proyectos.
        </p>
        
        <p style="color: #666666; line-height: 1.8;">
            En ARMAT desarrollamos departamentos modernos y funcionales en las mejores ubicaciones de la región.
        </p>
        
        <!-- Proyecto Destacado -->
        <div style="background: #F5F5F5; padding: 25px; margin: 30px 0;">
            <h3 style="color: #000000; margin: 0 0 10px 0;">ENTANYQ</h3>
            <p style="color: #666666; margin: 0 0 15px 0;">Departamentos en Centenario, Neuquén</p>
            <p style="color: #000000; font-weight: 600; margin: 0;">Desde USD 60.000</p>
        </div>
        
        <!-- CTA -->
        <div style="text-align: center; margin: 30px 0;">
            <a href="tel:2995089366" style="display: inline-block; background: #C9A96E; color: #000000; padding: 15px 40px; text-decoration: none; font-weight: 600; letter-spacing: 1px;">
                CONTACTANOS
            </a>
        </div>
        
        <p style="color: #666666; line-height: 1.8; font-size: 14px;">
            ¿Tenés alguna consulta? Respondé este email o llamanos al 299 508 9366.
        </p>
    </div>
    
    <!-- Footer -->
    <div style="background: #F5F5F5; padding: 30px; text-align: center;">
        <p style="color: #999999; font-size: 12px; margin: 0;">
            ARMAT Desarrolladora Inmobiliaria
        </p>
        <p style="color: #999999; font-size: 12px; margin: 5px 0 0 0;">
            299 508 9366 | @armat.desarrollos
        </p>
    </div>
    
</body>
</html>
```