# Third-party notices / Avisos de terceros

Esta carpeta contiene librerías de terceros fijadas para que el sitio funcione
sin conexión y sin depender de ningún CDN.

## three.js r128 (592 KB)

- Archivos: `three.min.js`, `GLTFLoader.js`, `OrbitControls.js`, `DRACOLoader.js`
- Origen: <https://github.com/mrdoob/three.js/tree/r128> (carga *examples/js*, no los
  módulos ES)
- Licencia: **MIT**
- Nota: se usa la versión antigua r128 a propósito, porque el proyecto está escrito
  contra la API clásica (`outputEncoding`, `sRGBEncoding`, `geometry` en vez de
  atributos). Migrar a three moderno es un trabajo aparte.

## Draco decoder

- Archivos: `draco/draco_decoder.wasm`, `draco/draco_wasm_wrapper.js`
- Origen: <https://github.com/google/draco> · versión publicada en
  <https://www.gstatic.com/draco/v1/decoders/>
- Licencia: **Apache License 2.0**
- Nota: `jimny.glb` declara `KHR_draco_mesh_compression`, así que el decodificador es
  obligatorio. Se omitió a propósito `draco_decoder.js` (704 KB), que solo se carga
  cuando `typeof WebAssembly !== 'object'`; ningún navegador moderno llega a esa rama.

## Modelo 3D

- Archivo: `../jimny.glb`
- "2018 Suzuki Jimny (unrefined version)" por @ShreyanshChaurasia_13
- <https://sketchfab.com/3d-models/2018-suzuki-jimny-unrefined-version-ee7a2a2d6a104fffadd3110044af2389>
- Licencia: **CC-BY 4.0** — se mantiene el crédito en el `<footer>` de `index.html`.

## Licencia de este proyecto

Sin archivo `LICENSE` por ahora. Si el proyecto se publica, conviene declarar la
licencia del código propio por separado de las librerías de terceros de arriba.