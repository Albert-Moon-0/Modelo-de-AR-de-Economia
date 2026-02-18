# 📊 AR Economía

Proyecto de Realidad Aumentada para presentar conceptos de economía.  
Funciona directamente en el navegador sin instalar ninguna app.

---

## 🗂️ Archivos del proyecto

| Archivo | Descripción |
|---|---|
| `index.html` | Experiencia AR principal |
| `marcadores.html` | Página para imprimir los marcadores |
| `README.md` | Este archivo |

---

> **Requisito importante**: el sitio **debe servirse por HTTPS** para que AR.js pueda acceder a la cámara. GitHub Pages lo hace automáticamente, así que no hay problema.

---

## 📱 Cómo usar el AR

1. Abre el enlace en un celular (Chrome o Safari)
2. Imprime la página `marcadores.html` (o ábrela en otra pantalla)
3. Pulsa **"Iniciar Cámara"** y acepta los permisos
4. Apunta la cámara al marcador desde ~25 cm de distancia
5. Espera 1-2 segundos y verás el panel flotando

---

## ✏️ Cómo agregar un nuevo concepto

### 1. En `index.html`, agrega un nuevo marcador en la sección AR:

```html
<a-marker preset="letterF" id="marker-nuevo" markerhandler="label: Tu Concepto">

  <!-- Panel de fondo -->
  <a-plane color="#1a2e1a" opacity="0.92" width="3" height="1.8"
           position="0 0.9 0" rotation="-90 0 0" material="side: double">
  </a-plane>

  <!-- Título -->
  <a-text value="TU CONCEPTO"
          color="#00ff88" align="center" width="2.8"
          position="0 1.75 0.01" rotation="-90 0 0"
          font="https://cdn.aframe.io/fonts/Exo2Bold.fnt" negate="false">
  </a-text>

  <!-- Separador -->
  <a-plane color="#00ff88" opacity="0.6" width="2.6" height="0.02"
           position="0 1.55 0.01" rotation="-90 0 0"></a-plane>

  <!-- Texto explicativo -->
  <a-text value="Escribe aquí tu explicación.\nPuedes usar \n para saltos de línea."
          color="#e0e0e0" align="center" width="2.5"
          position="0 1.3 0.01" rotation="-90 0 0" wrap-count="35">
  </a-text>

</a-marker>
```

### 2. En `marcadores.html`, agrega la tarjeta del marcador correspondiente.

---

## 🎯 Presets de marcadores disponibles

| Preset | Cómo usarlo en el código |
|---|---|
| HIRO | `preset="hiro"` |
| KANJI | `preset="kanji"` |
| Letra A | `preset="letterA"` |
| Letra B | `preset="letterB"` |
| Letra C | `preset="letterC"` |
| Letra D | `preset="letterD"` |
| Letra F | `preset="letterF"` |

Las imágenes de todos los marcadores están en:  
`https://github.com/AR-js-org/AR.js/tree/master/data/images`

---

## 💡 Consejos

- El marcador debe estar **bien iluminado** y **sin arrugas**
- Mantén la cámara **estable** unos segundos al apuntar
- Fondo contrastante (blanco o gris claro) ayuda a la detección
- Funciona mejor en **Chrome para Android** y **Safari para iOS**

---

## 🛠️ Tecnologías usadas

- [A-Frame](https://aframe.io/) — Framework de WebXR
- [AR.js](https://ar-js-org.github.io/AR.js-Docs/) — Librería de AR para el navegador
- GitHub Pages — Hosting gratuito
