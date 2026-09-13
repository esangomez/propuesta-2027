# Propuesta Académica 2026 — Colegio Santo Tomás

Versión web de la Propuesta Académica, pensada para leerse en el celular y para
que el contenido se pueda editar sin tocar el código.

Construida sobre el manual de marca del Colegio Santo Tomás (Eliana Tatángelo,
@demasiadografica).

## Qué incluye

```
contenido.js          todos los textos de la propuesta — es el archivo que se edita
index.html            diseño, maquetación y editor
assets/isotipo.svg    isotipo oficial, vectorial, en los cuatro colores corporativos
assets/fotos/         fotografías de la propuesta
```

## Dos versiones de la misma propuesta

Hay dos archivos HTML, y los dos muestran el mismo contenido de `contenido.js` —
no hay que mantener el texto en dos lugares.

- **`index.html`** — la versión para compartir. Es la que se abre en el link
  público (`https://esangomez.github.io/propuesta-2027/`). No tiene botón
  Editar ni ninguna herramienta de edición a la vista: es la que le mandás a
  una familia, ponés en el grupo de WhatsApp del colegio, o subís a
  santotomas.ar.

- **`editor.html`** — la misma propuesta con el editor completo: el botón
  Editar, los botones + y × para agregar o quitar ítems, y Exportar /
  Importar / Restablecer. Se abre en
  `https://esangomez.github.io/propuesta-2027/editor.html`. Es para vos,
  cuando querés probar un cambio de redacción antes de escribirlo
  directamente en `contenido.js`. Guardalo aparte en tus favoritos: no está
  enlazado desde ningún lado de la versión pública, a propósito.

## Publicar en GitHub Pages

1. Subir estos archivos a un repositorio (por ejemplo `propuesta-2026`).
2. Ir directo a `https://github.com/esangomez/propuesta-2026/settings/pages`.
   Es la vía más rápida. Si preferís navegar: pestaña **Settings** arriba del
   repositorio, y en la columna izquierda **Pages**, dentro del grupo
   *Code and automation*. Está bastante abajo en esa lista.
3. Ahí hay un bloque llamado **Build and deployment**, con dos desplegables.
   Le estás diciendo a GitHub de dónde tiene que sacar la página:
   - **Source** → elegir *Deploy from a branch*. Significa "publicá los archivos
     tal como están en el repositorio", sin ningún proceso previo. Es lo que
     corresponde acá, porque `index.html` ya está listo para abrirse.
   - **Branch** → elegir `main`. Es el nombre de la versión principal del
     repositorio, la única que vas a tener.
   - Al lado de `main` aparece un segundo desplegable con carpetas. Dejarlo en
     `/ (root)`, que quiere decir "la carpeta principal del repositorio". Ahí es
     donde está `index.html`. Si lo pusieras en `/docs`, GitHub buscaría la
     página dentro de una subcarpeta con ese nombre, que no existe.
   - Apretar **Save**.
4. A los dos minutos queda publicada en
   `https://esangomez.github.io/propuesta-2026/`.

Si no encontrás **Pages** en el menú, suele ser por una de estas dos razones:

- **El repositorio es privado.** Con una cuenta gratuita, Pages solo funciona en
  repositorios públicos. Se arregla en *Settings → General*, al final de la
  página, en *Change repository visibility*.
- **El repositorio está vacío.** Si todavía no subiste ningún archivo, la rama
  `main` no existe y el desplegable de *Branch* aparece sin opciones. Subí
  primero `index.html`, `README.md` y la carpeta `assets`, y volvé a Pages.

Para un dominio propio (por ejemplo `propuesta.santotomas.ar`), agregar un archivo
`CNAME` con ese nombre y apuntar el DNS a GitHub Pages.

## Editar el contenido

Todos los textos están en **`contenido.js`**. Es el único archivo que hay que
tocar para cambiar lo que se ve. `index.html` tiene el diseño y no hace falta
abrirlo nunca.

### Cambios chicos, directo en GitHub

1. Entrar al repositorio y abrir `contenido.js`.
2. Tocar el lápiz, arriba a la derecha.
3. Buscar el texto y cambiarlo.
4. Abajo, **Commit changes**. En dos minutos se ve en la web.

Funciona igual desde el celular.

Reglas para que no se rompa: el texto va entre comillas dobles, cada línea
termina en coma menos la última de cada bloque, y las comillas dobles dentro
de un texto se escriben `\"`. Si algo queda mal la página aparece en blanco;
se arregla deshaciendo el último cambio desde el historial del archivo.

### Cambios grandes, desde la página

Botón **Editar** en la propuesta: se modifica cualquier texto, se agregan o
quitan ítems y se cambian las fotos, viendo el resultado. Eso queda guardado
solo en ese navegador. Para publicarlo: **Exportar contenido**, **Copiar**, y
pegar en `contenido.js` reemplazando todo lo que haya. Lo que copia el botón
ya viene con la forma exacta del archivo.

### Los dos niveles

`contenido.js` tiene un bloque `niveles` con `primaria` y `secundaria`. Cada
uno lleva su arancel, su horario, sus materias, su informe y su uniforme. El
resto de la propuesta —misión, equipo, recursos, documentación, inscripción y
contacto— es común a los dos.

Los aranceles están en `niveles` → `primaria` (o `secundaria`) → `arancel`.
Son cuatro líneas: el rótulo, el monto, qué incluye y desde cuándo rige.
Cuando cambien los valores, actualizá también la línea `vigencia`.

## Logos de plataformas

La sección Comunicación y la sección Recursos muestran el logo de las
plataformas que usa el colegio: Handing, Google Workspace, Smart Team, PATH
Examinations, Kapelusz y Aprendo Leyendo. Esos archivos todavía no están
cargados — hoy se ven solo el nombre, sin ícono, porque el diseño está armado
para no romperse mientras faltan.

Para agregarlos: **Editar**, y sobre cada nombre aparece un botón **Agregar
logo**. Sirve un PNG con fondo transparente, del sitio oficial de cada marca.
Subilo igual que una foto, o pegá un enlace si ya está publicado en algún
lado. El logo se ve chico — no hace falta alta resolución, con 200×200 px
alcanza de sobra.

## Publicar cambios sin pasar por GitHub

En `editor.html` hay un botón **Publicar en GitHub**, al lado de Exportar
contenido. Sube los cambios directamente, sin copiar y pegar nada a mano.

La primera vez pide un token: una clave que generás vos, con permiso
solamente sobre este repositorio.

1. Entrá a [github.com/settings/personal-access-tokens/new](https://github.com/settings/personal-access-tokens/new).
2. En **Repository access**, elegí **Only select repositories** y
   seleccioná `propuesta-2027`. No le des acceso a ningún otro repositorio.
3. En **Permissions → Repository permissions → Contents**, elegí
   **Read and write**. Es el único permiso que necesita.
4. Ponele una fecha de vencimiento — un año está bien — y generalo.
5. GitHub te muestra el token una sola vez. Copialo y pegalo en el cuadro
   de **Publicar en GitHub**.

Ese token es como una contraseña: quien lo tenga puede modificar este
repositorio. Nunca queda escrito en ningún archivo — la página lo pide cada
vez, salvo que tildes **Recordar el token en este navegador**, y en ese caso
queda guardado solamente en tu propio navegador, nunca en GitHub. Si en algún
momento lo perdés de vista o creés que alguien más lo tiene, entrá a
[github.com/settings/tokens](https://github.com/settings/tokens) y
revocalo — se genera uno nuevo en un minuto.

Este botón vive únicamente en `editor.html`. La versión pública,
`index.html`, no lo tiene ni tiene forma de tenerlo.

## Aplicación del manual de marca

### Paleta corporativa

| Color | Hex | Uso en la pieza |
|---|---|---|
| Azul | `#00669c` | logotipo, jornada, inscripción, cierre |
| Celeste | `#55a1d9` | uniforme, talleres de verano |
| Rojo | `#e41a22` | año en portada, materias extracurriculares, beneficios |
| Verde | `#50b32b` | comedor, aranceles |
| Naranja | `#f99c02` | misión, medios de pago, contacto |
| Violeta | `#8f3f9c` | compromiso, equipo, materiales, documentación |
| Fondo | `#f4edec` | secciones alternas y portada |

Los seis colores se aplican sin variaciones, como pide el manual. Cada sección
toma uno como color de acento, de modo que el color cumple una función de
orientación y no de decoración.

### Tipografías

| Familia | Rol |
|---|---|
| M PLUS Rounded 1c | solo el logotipo, nunca texto corrido |
| Fraunces | títulos y números destacados |
| Gladiola | frases manuscritas: la cita de portada, la de Montessori, el cierre |
| Livvic | texto de corrido, listas, botones |

Gladiola es una tipografía paga de Melvastype y no está en Google Fonts, así que
no se puede servir desde la web. La pieza la pide primero: si quien mira la
página la tiene instalada, la ve; si no, cae en **Caveat Brush**, un pincel
gratuito de proporciones parecidas. Son cuatro frases en toda la propuesta.
Fraunces, Livvic y M PLUS Rounded 1c sí se cargan desde Google Fonts.

### Isotipo

`assets/isotipo.svg` es el archivo oficial de la carpeta de marca, en vectorial:
escala sin pixelarse en cualquier pantalla y sirve también de favicon. Se aplica
sobre fondo claro y sobre azul con una caja blanca detrás, para respetar el
contraste que pide el manual.

## Pendiente

- La cita de portada, de María Elena Walsh, viene del folleto anterior. Conviene
  revisar si sigue representando a la marca nueva.
- Sumar fotografías institucionales en talleres y uniforme.
- Si querés el logotipo completo (isotipo + nombre + bajada) en la portada en
  lugar del isotipo solo, está en la carpeta de marca como
  `Logotipo/Vectoriales/svg/Santo Tomás-01.svg`.
