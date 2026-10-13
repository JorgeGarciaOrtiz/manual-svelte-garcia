# Manual introductorio de Svelte

Práctica 1 de OPT: manual introductorio de Svelte con un ejemplo de lista de tareas.

**Autor:** Jorge García Ortiz, 2º DAW

## Contenido del repositorio

- `Manual_Svelte.pdf`: el manual.
- `ejemplo/`: proyecto SvelteKit con la lista de tareas.

## Cómo ejecutar el ejemplo

### Requisitos

- Node.js 24 o superior (con npm). Yo he usado Node.js 24.21.0 y npm 11.19.0.
- Un navegador web.

### Pasos

```bash
git clone https://github.com/JorgeGarciaOrtiz/manual-svelte-garcia.git
cd manual-svelte-garcia/ejemplo
npm install
npm run dev
```

Abre en el navegador la dirección que muestra la terminal, normalmente <http://localhost:5173/>.

## Qué hace el ejemplo

Una lista de tareas: escribes un texto en el campo, pulsas **Añadir** y la tarea aparece en la lista. El código está en `ejemplo/src/routes/+page.svelte`.