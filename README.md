# Marcador HEMA

Marcador de una sola página para combates de HEMA. Es HTML/CSS/JS estático, sin build ni base de datos. El estado se guarda en el `localStorage` del navegador, así que recargar la página no borra el combate.

## Funciones

- Puntos +1 / +2 / +3 / −1 por luchador, con nombres editables
- Temporizador configurable con aviso sonoro al terminar
- Contador de dobles con máximo configurable
- Amonestaciones y penalizaciones
- Puntos para ganar (se detiene el reloj y se marca al ganador)
- Deshacer, pantalla completa y atajos de teclado (ver ⚙ Ajustes)

## Uso local

Abre `public/index.html` en el navegador, o sirve la carpeta:

```sh
npx serve public
```

## Publicar en Cloudflare Pages

**Opción A: desde Git (despliegue automático en cada push)**

1. Sube este repositorio a GitHub o GitLab.
2. En Cloudflare: *Workers & Pages → Create → Pages → Connect to Git*.
3. Configuración de build:
   - Framework preset: `None`
   - Build command: *(vacío)*
   - Build output directory: `public`

**Opción B: desde la terminal con Wrangler**

```sh
npx wrangler login
npx wrangler pages deploy public --project-name marcador-hema
```
