# Memoria TFG GIC Jorge Contreras

Memoria del trabajo de fin de grado de Ingeniería de Computadores.

## Trabajar con LaTeX

### Instalación de LaTeX

Para trabajar con LaTeX es necesario instalar una distribución de LaTeX (se recomienda [TeX Live](https://www.tug.org/texlive/))

* [Instalar en Linux](https://www.tug.org/texlive/quickinstall.html)
* [Instalar en Windows](https://www.tug.org/texlive/windows.html)
* [Instalar en MacOS](https://www.tug.org/mactex/)

### Instalación del IDE + Plugins

Para editar la memoria, se recomienda utilizar [VSCode](https://code.visualstudio.com/) haciendo uso de las siguientes extensiones: 

* [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)
* [LaTeX language support](https://marketplace.visualstudio.com/items?itemName=torn4dom4n.latex-support)

#### Instalación con Docker (opcional)

Haciendo uso de la extensión _LaTeX Workshop_ también es posible dockerizar todos los paquetes LaTeX:

1. Teniendo [Docker](https://www.docker.com/) instalado, descargamos una imagen que contenga los paquetes LaTeX:

```
$ docker pull tianon/latex
```

2. Abrir el archivo _settings.json_ de VSCode (Ctrl + Shift + P > Preferences: Open Settings) y añadir las siguientes lineas:

```
{
    "latex-workshop.docker.enabled": true,
    "latex-workshop.latex.outDir": "./out",
    "latex-workshop.synctex.afterBuild.enabled": true,
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.docker.image.latex": "tianon/latex",
}
```

Los archivos resultantes estarán situados en la carpeta `out/`
