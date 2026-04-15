# Prueba Lectiva

Base SvelteKit con arquitectura `feature-first/domain-first` para integrar la API de Rick and Morty.

## Run

```bash
npm install
npm run dev
```

## Check

```bash
npm run check
npm run build
```

## CI/CD

El repositorio incluye dos workflows de GitHub Actions:

- `CI`: instala dependencias, ejecuta `npm run check` y valida el build en cada `push` a `main` y en cada `pull_request`.
- `Deploy to GitHub Pages`: compila el sitio estatico y lo publica en GitHub Pages cuando hay cambios en `main`.

Para activar el despliegue:

1. En GitHub entra a `Settings > Pages`.
2. En `Source`, selecciona `GitHub Actions`.
3. Haz push a `main` y el workflow publicara el sitio automaticamente.

## Estructura

- `src/lib/core`: cliente HTTP, configuracion y adaptadores.
- `src/lib/entities`: tipos y mapeos de dominio.
- `src/lib/features`: features por caso de uso.
- `src/routes`: composicion de rutas y carga de datos.
