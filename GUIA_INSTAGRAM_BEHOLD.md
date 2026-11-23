# Guía de Integración: Auto-mostrar fotos de Instagram con Behold.so

Esta guía te explica paso a paso cómo conectar tu cuenta de Instagram con **[Behold.so](https://behold.so)** para que las fotos de tu perfil aparezcan de forma **100% automática** en la sección **Galería** de tu landing page, sin necesidad de programar ni tocar código continuamente.

---

## ¿Por qué Behold.so?

- **Plan Gratuito Permanente**: Te permite conectar 1 cuenta y mostrar tus publicaciones más recientes.
- **Sin Servidor ni Backend**: No requiere renovar tokens manuales de Facebook cada 60 días (Behold lo hace automáticamente en segundo plano).
- **Rápido y Seguro**: Solo solicita permisos de lectura de tus publicaciones públicas.
- **Se adapta a tu diseño**: Podemos configurarlo para que muestre únicamente las fotos limpias en cuadrícula de 3 columnas, coincidiendo con el estilo de *Jungle Sound System*.

---

## Paso 1: Crear tu cuenta en Behold

1. Ingresa a **[https://behold.so](https://behold.so)**.
2. Haz clic en el botón **"Sign Up"** o **"Get Started for Free"**.
3. Regístrate con tu correo electrónico o mediante tu cuenta de Google.

---

## Paso 2: Vincular tu cuenta de Instagram

1. Una vez dentro de tu panel de Behold (*Dashboard*), haz clic en **"Connect Instagram"** o **"Add Account"**.
2. Selecciona el tipo de cuenta:
   - **Personal Account** (si tu cuenta es personal/estándar).
   - **Creator / Business Account** (si tu cuenta es profesional o de empresa).
3. Se abrirá la ventana oficial de Meta/Instagram pidiéndote autorización.
4. Inicia sesión en tu cuenta de Instagram y pulsa **"Permitir"** (*Allow*).

> **Nota de seguridad:** Behold solo solicita permisos de **lectura**. Nunca tendrá acceso a tus contraseñas, mensajes directos ni podrá publicar en tu nombre.

---

## Paso 3: Crear y configurar tu Feed

1. En el panel de Behold, haz clic en **"Create a Feed"**.
2. Dale un nombre (por ejemplo: `Jungle Sound System Web`).
3. Elige el estilo de visualización:
   - **Layout**: Selecciona **Grid** (cuadrícula).
   - **Columns**: Elige **3 columnas** para escritorio y **1 o 2** para móvil.
   - **Number of Posts**: Puedes elegir 6 o 9 fotos.
   - **Show text / captions**: **Desmárcalo** para que solo se muestren las imágenes limpias, tal como lo solicitaste.
4. Haz clic en **"Save Feed"**.

---

## Paso 4: Obtener tu código de inserción (Embed Code)

En la parte superior derecha de tu Feed en Behold, haz clic en el botón **"Embed Code"**.

Verás un código muy corto similar a este:

```html
<figure data-behold-id="AQUI_VIENE_TU_ID_DE_BEHOLD"></figure>
<script src="https://w.behold.so/widget.js" type="module"></script>
```

Copia ese código o guarda tu **Feed ID** (el código de letras y números que aparece dentro de `data-behold-id="..."`).

---

## Paso 5: Cómo insertarlo en la página web

Para integrarlo en tu landing page:

1. Abre tu archivo `code.html`.
2. Busca la sección `<section ... id="galeria">`.
3. Dentro de `<div id="galleryGrid">`, simplemente reemplazas las 6 tarjetas de prueba por tu etiqueta de Behold:

```html
<!-- GALERÍA AUTOMATIZADA CON BEHOLD.SO -->
<div class="w-full relative z-10" id="galleryGrid">
  <figure data-behold-id="TU_ID_AQUI"></figure>
  <script src="https://w.behold.so/widget.js" type="module"></script>
</div>
```

> **Opción fácil:** Cuando tengas tu ID de Behold, simplemente pégalo aquí en el chat diciéndome: *"Este es mi ID de Behold: [TU_ID]"* y yo mismo lo integraré y ajustaré los estilos en `code.html` por ti.

