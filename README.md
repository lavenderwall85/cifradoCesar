# sv

Everything you need to build a Svelte project, powered by [`sv`](https://github.com/sveltejs/cli).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npx sv create

# create a new project in my-app
npx sv create my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.

Descifrador César

¿Qué hace?

* Esta aplicación te ayuda a descifrar mensajes secretos que fueron cifrados usando el método César. Solo necesitas ingresar el mensaje, ajustar un número, y listo, te muestra el mensaje original.

¿Cómo se usa tu aplicación?

* Escribe el mensaje cifrado en el primer cuadro.
* Mueve el deslizador para elegir el número de desplazamiento.
* Presiona el botón "DESCIFRAR".
* Mira el mensaje descifrado en el cuadro de abajo.

¿Cómo la hiciste?

* Usé Svelte para hacer la aplicación porque me gusta cómo funciona.
Dibujé la parte visual (campos, botones, etc.) con HTML y le puse algo de estilo con CSS.
Hice que descifrara los mensajes con un código que cambia cada letra según el número que pongas en el deslizador.

Algo que aprendí

* Me sirvió para entender mejor cómo funcionan los números y las letras en el código, y cómo conectar todo para que se vea y funcione bien.