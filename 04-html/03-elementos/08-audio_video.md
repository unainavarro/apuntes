<h1 align="center">Audio y Video</h1>

<h2>📑 Contenido</h2>

- [Videos](#videos)
- [Audio](#audio)
- [Track](#track)

## Videos

El elemento `<video>` se utiliza para insertar videos. La etiqueta `<video>` puede envolver las etiquetas `<source>`. Las etiquetas `<source>` nos facilita crear una lista con varios formatos compatibles para el video que queremos insertar.

```html
<!-- Ejemplo Video -->
<video width="320" height="240" controls>
  <source
    src="https://player.vimeo.com/external/567282335.sd.mp4?s=6b36bda539f3a3fb1f6106160d843de81b8bae86&profile_id=165&oauth2_token_id=57447761"
  />
  <source src="video/otro/formato.mp4" type="video/mp4" />
  <source src="video/otro/formato.ogg" type="video/ogg" />
  La etiqueta video no es compatible con tu navegador
</video>
```

**Atributos más usados:**

- **src:** Especifica la ruta del video.
- **controls:** Visualizar panel de controles.
- **poster:** Insertar una imagen de portada.
- **autoplay:** Se reproduce de manera automática.
- **loop:** Se reproduce en bucle.
- **muted:** Aparece en modo silencio.
- **preload:** Inicia la descarga y almacenamiento en el buffer del vídeo.

## Audio

El elemento `<audio>` funciona de la misma manera que el elemento video, comparten la gran mayoría de atributos.

```html
<!-- Ejemplo Audio -->
<audio controls>
  <source src="ruta/del/audio.ogg" type="audio/ogg" />
  <source src="ruta/del/audio.mp3" type="audio/mpeg" />
</audio>
```

## Track

La etiqueta `<track>` se usa para añadir pistas de texto a elementos de medios como `<video>` y `<audio>`. Las pistas de texto pueden ser subtítulos, títulos, descripciones, capítulos o metadatos.

**Atributos más usados:**

- **src:** Especifica la ruta del video.
- **srclang:** Código de idioma ISO 639-1 de los subtítulos.
- **label:** Título que verá el usuario para elegir al pulsar en el botón CC.
- **kind:** Indica el tipo o género de subtítulos enlazados
- **default(boolean):** Marca este canal como los subtítulos principales por defecto.

```html
<!-- Ejemplo Track -->
<video width="320" height="240" controls>
  <source src="mi-video.mp4" type="video/mp4" />
  <source src="mi-video.ogg" type="video/ogg" />
  <track src="mi-sub.vtt" kind="subtitles" srclang="en" label="English" />
  <track src="mi-sub.vtt" kind="subtitles" srclang="es" label="Español" />
</video>
```
