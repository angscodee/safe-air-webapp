# 📹 Video Demo - Aire Seguro, Hogar Seguro

## 📂 Ubicación de Videos

Coloca tus videos demo en esta carpeta:

```
webapp/assets/videos/
├── demo-principal.mp4
├── demo-simulacion.mp4
├── demo-alertas.mp4
└── README.md (este archivo)
```

## 🎬 Tipos de Videos Recomendados

### 1. **demo-principal.mp4**
**Duración**: 2-3 minutos  
**Contenido**:
- Intro a la plataforma
- Selección de entorno (Restaurante/Hogar)
- Vista general de zonas
- Navegación básica

### 2. **demo-simulacion.mp4**
**Duración**: 1-2 minutos  
**Contenido**:
- Apertura del simulador
- Selección de zona y escenario
- Ejecución de simulación
- Cierre automático de válvulas
- Visualización de cambios en tiempo real

### 3. **demo-alertas.mp4**
**Duración**: 1-2 minutos  
**Contenido**:
- Centro de alertas activas
- Protocolo de seguridad
- Reconocimiento de alertas
- Vista de historial con timeline

## 🔗 Uso del Video en la Webapp

### Opción 1: Video en Pantalla de Bienvenida

Agrega el video como fondo o en la sección "Ver cómo funciona":

```html
<!-- En index.html o experience.html -->
<video 
  src="assets/videos/demo-principal.mp4" 
  controls 
  poster="assets/videos/poster.jpg"
  style="max-width: 100%; border-radius: 12px;">
</video>
```

### Opción 2: Modal de Video

Al hacer clic en "Ver cómo funciona":

```javascript
function showHow() {
  // Mostrar modal con video embebido
  const modal = document.createElement('div');
  modal.className = 'modal-overlay';
  modal.innerHTML = `
    <div class="modal" style="max-width: 900px;">
      <div class="modal-header">
        <h2>Cómo Funciona el Sistema</h2>
      </div>
      <div class="modal-body">
        <video 
          src="assets/videos/demo-principal.mp4" 
          controls 
          autoplay
          style="width: 100%; border-radius: 8px;">
        </video>
      </div>
      <div class="modal-footer">
        <button class="btn btn-secondary" onclick="this.closest('.modal-overlay').remove()">
          Cerrar
        </button>
      </div>
    </div>
  `;
  document.body.appendChild(modal);
}
```

### Opción 3: YouTube/Vimeo Embed

Si subes el video a YouTube o Vimeo:

```html
<!-- YouTube -->
<iframe 
  width="100%" 
  height="500" 
  src="https://www.youtube.com/embed/TU_VIDEO_ID" 
  frameborder="0" 
  allowfullscreen>
</iframe>

<!-- Vimeo -->
<iframe 
  src="https://player.vimeo.com/video/TU_VIDEO_ID" 
  width="100%" 
  height="500" 
  frameborder="0" 
  allowfullscreen>
</iframe>
```

## 📱 Consideraciones para Móviles

- **Tamaño del video**: Mantener archivos < 50MB para carga rápida
- **Formato**: MP4 con codec H.264 (máxima compatibilidad)
- **Resolución**: 1920x1080 (Full HD) o 1280x720 (HD)
- **Autoplay**: En móvil NO funciona con sonido (requiere `muted`)
- **Poster**: Siempre incluir una imagen poster (primer frame del video)

## 🎨 Ejemplo Completo de Integración

```html
<!-- Sección de Video en Home -->
<section class="video-demo" style="padding: 4rem 2rem; text-align: center;">
  <h2 style="font-size: 2rem; margin-bottom: 1rem;">
    Ve el Sistema en Acción
  </h2>
  <p style="color: var(--text-secondary); margin-bottom: 2rem;">
    Descubre cómo funciona la detección temprana de fugas
  </p>
  
  <div style="max-width: 900px; margin: 0 auto;">
    <video 
      id="demoVideo"
      src="assets/videos/demo-principal.mp4" 
      poster="assets/videos/poster.jpg"
      controls
      preload="metadata"
      style="
        width: 100%; 
        border-radius: 16px; 
        box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        border: 1px solid var(--border-color);
      ">
      Tu navegador no soporta el tag de video.
    </video>
  </div>
  
  <div style="margin-top: 2rem;">
    <button class="btn btn-primary" onclick="startExperience()">
      Probar Ahora
    </button>
  </div>
</section>
```

## 🚀 Hosting de Videos

### Opción 1: En el repositorio (No recomendado)
- ❌ Aumenta el tamaño del repo
- ❌ Lento para clonar
- ✅ Control total

### Opción 2: GitHub Releases
- ✅ No aumenta el tamaño del repo
- ✅ CDN de GitHub
- ✅ Versionado

### Opción 3: YouTube/Vimeo (Recomendado)
- ✅ Streaming optimizado
- ✅ Sin límite de tamaño
- ✅ Analytics incluidos
- ✅ Subtítulos automáticos

### Opción 4: Cloudinary/Vercel
- ✅ CDN global
- ✅ Optimización automática
- ✅ Adaptive streaming

## 📝 Checklist de Video

Antes de publicar el video, verifica:

- [ ] Formato MP4 H.264
- [ ] Resolución 1080p o 720p
- [ ] Audio claro y balanceado
- [ ] Subtítulos en español (opcional)
- [ ] Tamaño < 50MB (comprimido)
- [ ] Imagen poster generada
- [ ] Probado en Chrome, Firefox, Safari
- [ ] Probado en móvil
- [ ] Sin información sensible visible

## 🎬 Herramientas de Edición

### Gratuitas:
- **DaVinci Resolve** (profesional)
- **OpenShot** (simple)
- **Shotcut** (intermedio)

### Online:
- **Clipchamp** (Microsoft)
- **Kapwing**
- **VEED.io**

### Para Screen Recording:
- **OBS Studio** (gratis, profesional)
- **ShareX** (Windows)
- **Loom** (online, fácil)

## 📊 Métricas Sugeridas

Si usas YouTube/Vimeo, monitorea:
- Tasa de retención
- Tiempo promedio de visualización
- Click-through rate (CTR) al botón de prueba
- Comentarios/feedback

---

**Nota**: Los videos deben mostrar la plataforma de forma honesta, sin funcionalidades inventadas. Marca claramente que es una simulación cuando corresponda.
