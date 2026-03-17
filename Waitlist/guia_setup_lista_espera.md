# Soulmigo — Landing Page de Lista de Espera: Guía de Configuración

**Objetivo:** Capturar correos electrónicos antes del lanzamiento en Amazon en septiembre de 2026.  
**Coste:** £0  
**Tiempo:** 2–3 horas en total (la primera vez)  
**Resultado:** Una página activa en `soulmigo.co.uk` donde la gente se registra para obtener acceso anticipado.

---

## Resumen: Cómo Funciona

```
El visitante llega a soulmigo.co.uk
        |
        v
Ve la landing page de la lista de espera (archivo HTML, alojado en Netlify)
        |
        v
Rellena su email y envía el formulario
        |
        v
El email se captura en Mailchimp (o Google Sheets si usas Google Form)
        |
        v
Les envías un email el día del lanzamiento con un código de descuento
```

---

## Opción A — Mailchimp (Recomendada)

La mejor opción porque:

- Gratis hasta 500 suscriptores.
- Te permite enviar un email de lanzamiento a todos los de la lista con un solo clic.
- Se integra directamente en el formulario HTML sin necesidad de backend.

### Paso 1 — Crear una cuenta en Mailchimp

1. Ve a [mailchimp.com](https://mailchimp.com) y regístrate (gratis).
2. Completa la configuración: nombre de marca "Soulmigo", sitio web `soulmigo.co.uk`.
3. En el panel, ve a **Audience → Audience dashboard → Signup forms → Embedded forms**.
4. Copia la URL de `action` del código del formulario. Se ve así:

   ```
   https://soulmigo.us21.list-manage.com/subscribe/post?u=XXXX&id=YYYY
   ```

5. Guarda esa URL — la pegarás en el archivo HTML.

### Paso 2 — Crear la landing page HTML

1. Crea un archivo llamado `index.html` en tu ordenador.
2. Pega la plantilla HTML de la lista de espera de Soulmigo (crearemos este archivo a continuación).
3. Reemplaza el marcador `ACTION_URL_HERE` en la etiqueta de formulario con tu URL de Mailchimp del Paso 1.

### Paso 3 — Alojar en Netlify (gratis)

1. Ve a [netlify.com](https://netlify.com) y regístrate (gratis).
2. En el panel, haz clic en **"Add new site" → "Deploy manually"**.
3. Arrastra y suelta tu archivo `index.html` (o la carpeta que lo contiene) en el área de carga.
4. Netlify te dará una URL temporal como `https://nombre-aleatorio-123.netlify.app` — la página ya está activa.
5. Puedes probarla inmediatamente en esa URL.

### Paso 4 — Conectar tu dominio `soulmigo.co.uk`

1. En Netlify, ve a **Site settings → Domain management → Add custom domain**.
2. Escribe `soulmigo.co.uk` y confirma.
3. Netlify te mostrará los registros DNS que debes añadir (normalmente dos registros: `A` y `CNAME`).
4. Inicia sesión en tu registrador de dominios (donde compraste el dominio).
5. Ve a **Configuración DNS** y añade los registros que te dio Netlify.
6. Espera de 15 a 60 minutos para que el DNS se propague.
7. Visita `soulmigo.co.uk` — tu página debería aparecer.

**El SSL (HTTPS) es automático y gratuito** — Netlify lo gestiona a través de Let's Encrypt.

---

## Opción B — Google Form (Más simple, menos potente)

Usa esto si no quieres configurar Mailchimp todavía.

### Paso 1 — Crear el formulario

1. Ve a [forms.google.com](https://forms.google.com).
2. Crea un nuevo formulario. Título: **"Soulmigo Early Access"**.
3. Añade una pregunta: **"Tu dirección de correo electrónico"** — tipo: Respuesta corta. Márcala como obligatoria.
4. Pregunta opcional: **"¿Para qué usas calcetines de yoga?"** (yoga / pilates / ambos) — tipo: Opción múltiple.
5. En Configuración → Respuestas, activa **"Recopilar direcciones de correo electrónico"**.
6. Haz clic en el botón **Enviar** y copia el enlace.

### Paso 2 — Compartir el enlace

- Pega el enlace de Google Form en:
  - Tu bio de TikTok (como enlace en la bio).
  - Tu bio de Instagram.
  - El pie de foto o CTA de cada vídeo de TikTok hasta el lanzamiento.

---

## Contenido de la Landing Page (texto a usar)

Headline:
> Calcetines de yoga que realmente agarran.

Subheadline:
> Soulmigo — calcetines de yoga de algodón orgánico con agarre anatómico de 3 zonas.  
> Hechos para mujeres que se toman en serio su práctica.  
> Lanzamiento en septiembre de 2026.

Etiqueta del formulario:
> Únete a la lista de espera para acceso anticipado y precios de lanzamiento.

Botón:
> Unirme a la lista

Texto pequeño debajo del botón:
> Sin spam. Un solo email cuando lancemos. Date de baja cuando quieras.

---

## Colores de Marca para la Página

| Rol | Hex |
|-----|-----|
| Fondo | `#F5F0EB` (blanco roto cálido) |
| Texto principal | `#2C2C2C` (carbón) |
| Fondo del botón | `#2D5F3E` (verde bosque) |
| Texto del botón | `#F5F0EB` (blanco roto) |
| Acento / detalle | `#C4704B` (terracota) |

Tipografía: **Inter** (gratis vía Google Fonts).

---

## Dónde compartir el enlace

Una vez que la página esté activa en `soulmigo.co.uk`:

- **TikTok:** "Enlace en la bio" — añade el dominio a tu perfil. Menciónalo en el CTA de cada vídeo.
- **Instagram:** Lo mismo — enlace en la bio. Añádelo a cada story.
- **Captions:** Termina los vídeos con: "Únete a la lista de espera — enlace en la bio".

---

## Email de Lanzamiento (Borrador)

**Asunto:** Tus Soulmigo ya están aquí — aquí tienes tu descuento de acceso anticipado

> Hola,
>
> Te uniste a la lista de espera de Soulmigo en mayo. Hoy es el día.
>
> Nuestros calcetines de yoga de algodón orgánico con agarre anatómico de 3 zonas ya están a la venta en Amazon UK.
>
> Como agradecimiento por la espera, usa el código **EARLYACCESS15** para obtener un 15% de descuento en tu primer pedido.
>
> [Comprar en Amazon →] [enlace]
>
> Gracias por confiar en Soulmigo desde el principio.
>
> — Equipo Soulmigo, Glasgow
