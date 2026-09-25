# Cyber Maze: Pursuit Protocol

## Ejecucion con Node.js
Este proyecto incluye un servidor Node.js real para servir `index.html`, CSS, JavaScript, imagenes y el MP3.

### Requisitos
- Node.js 18 o superior
- Navegador moderno

### Iniciar
En Windows puedes ejecutar `ABRIR_JUEGO.bat`.

O manualmente:
```bash
npm start
```
Despues abre:
`http://localhost:3010`

### Musica
La pista principal es `assets/audio/cybermaze-theme.mp3`. Se reproduce en bucle cuando el usuario pulsa `INICIAR MISION`. El servidor incluye el tipo MIME `audio/mpeg`, por lo que el navegador puede cargar correctamente el MP3 por HTTP.

### Controles
- WASD / flechas: movimiento
- Espacio / Enter: ataque/accion
- P: pausa
- R: reiniciar
- F2: debug
- M: activar/desactivar audio

### Estructura
- `index.html`: interfaz
- `css/styles.css`: estilos
- `js/cybermaze.js`: logica principal
- `assets/`: musica, fondos y sprites
- `server/server.js`: servidor HTTP Node.js y endpoints de datos
- `server/data/`: almacenamiento del ranking/niveles del servidor

### Node.js
Node.js se utiliza como servidor local. El navegador sigue ejecutando el gameplay en JavaScript, mientras Node.js entrega los archivos y expone `/api/scores` y `/api/levels`.
