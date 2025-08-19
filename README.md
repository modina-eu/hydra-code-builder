SFDCANBAC-UX
========

Web demo (via render dot com):

https://hydra-code-builder.onrender.com

(Recommended use in Chrome)

Graphical interface to procedurally generate Hydra code via the selection of visual inputs and modifiers; these continuously pass through a neural network, modelled to provide parameter inputs for endless visual manipulation. In turn, the code can be used to alter movements viewed from a live camera feed.

![demo screenshot](https://modina.eu/wp-content/uploads/2025/08/Screenshot-2025-08-19-at-17.25.37-scaled.png)

Code by [naoto hieda](https://naotohieda.com)

### Notes for porting from glitch.me to render.com

- Change node version to 22.12 in `package.json`

```
"scripts": {
  "start": "vite build --watch --emptyOutDir & vite",
  "build": "vite build",
  "serve": "vite preview"
},
```

```  
"engines": {
    "node": "22.12"
  }
```

- Edit `vite.config.js`, change url accordingly
```
preview: {
  allowedHosts: ['hydra-code-builder.onrender.com'],
},
```

- In render.com Web Service settings
  - **Build Command:**
  `npm install -D vite && npm run build`
  - **Start Command:**
  `npm run serve`
