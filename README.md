# AZUL INFINITO 🕯️

Roguelike 2D top-down estilo *The Binding of Isaac*: 6 pisos procedurales, folk-horror analógico, CRT, co-op LAN y en línea con salas por código.

## Jugar

- **Local:** abre `index.html` en Chrome/Edge (doble clic).
- **Localhost:** `npx serve .` (o cualquier servidor estático) → http://localhost:3000
- **Publicar:** sube este repo/carpeta como juego HTML a [itch.io](https://itch.io).

## Controles

| Tecla | Acción |
|---|---|
| `WASD` | Moverse |
| `←↑↓→` | Llorar / disparar |
| `ESPACIO` | Bomba de carne |
| `R` | Reencarnar (nuevo piso, solo host) |
| `Enter` | Empezar |

## Co-op

- **En línea:** `Crear sala` → comparte el código de 5 letras → el otro PC lo escribe y pulsa `Unirse`.
- **LAN sin internet:** `Host LAN` / `Unirse` con códigos largos copiar-pegar.
- El host simula la partida; cada jugador tiene su propia build de pasivas. Si uno cae, el otro lo revive limpiando la sala.

## Estructura (un solo archivo)

Todo el juego vive en `index.html`: generación procedural (start/normal/tesoro/tienda/jefe), inventario (HP, monedas, bombas, llaves), 12 enemigos + 6 jefes con máquinas de estados, 8 pasivas de lágrimas, 6 pisos con trampilla, y netcode WebRTC/PeerJS (~20 snapshots/s).
