

# BlogKit Base Theme
This theme comes with BlogKit, and is a great starting point for creating your own theme.

### Create your theme
Fork this repository, and take a look at the available components (in /src/lib). If you see a component you wish to change, you can do so by adjusting the HTML (sans Svelte tags) in [the Tailwind Playground](https://play.tailwindcss.com/) until you are satisfied. Once you are finished, copy the resulting HTML, replacing any missing svelte directives.

### Customize Tailwind
BlogKit natively comes with Tailwindcss, and this is what you are expected to theme your site in. You can edit `src/lib/app.css` and `src/lib/tailwind.js` to edit tailwind configurations. 

### Deploying
To deploy your theme, publish it to NPM (*If you wish your theme to be published into the BlogKit organization, reach out to a maintainer*) and set your `VITE_BK_THEME` ENV var to your NPM package.

**REMINDER**: You must rebuild a BlogKit app after changing the theme environment variable.