# Bachelor Thesis regarding COVID-19 Data Visualizations
The following thesis is focused on COVID-19 Data Visualization. It does explore this medium by creating a customizable Dashboard for Millennials. A Jupyter Notebook was created to determine which Visualization Types should be explored. The Jupyter Notebook can be found [here](https://github.com/YahArt/covid-jupyter-notebook-fhgr).

The Dashboard is written as an Angular Web Application. Furthermore a Flask based REST API for Data Processing was implemented. The Dasbhoard can be found [here](https://github.com/YahArt/covid-pydash/).

## How to compile
The thesis is written in `latex with Overleaf`. As Overleaf comes with a price tag the instructions below provide a starting point in order to generate a pdf file with the free tool VS Code.
### Prerequisites
* Download and install VS Code from [here](https://code.visualstudio.com/)
* Make sure you have a full featured latex setup ready. For Linux you can simply install `textlive-most` with your favorite package manager. For Windows the `TextLive` distribution is recommended which can be found [here](https://tug.org/texlive/windows.html#install)
* Install the `LaTeX Workshop` extension in VS Code which can be found [here](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).

### Configure LaTeX Workshop
Open your Settings.json file in VsCode to do so simply press `Ctrl + Shift + P` and search for `Settings`. Append the following configuration options:
```json
"editor.formatOnSave": true,
"latex-workshop.latex.recipes":[
    {
        "name": "pdflatex, makeglossaries, bibtex, pdflatex (2x)",
        "tools": [
            "pdflatex",
            "makeglossaries",
            "bibtex",
            "pdflatex",
            "pdflatex"
        ]
    },
],
"latex-workshop.latex.tools":[
    {
        "name": "pdflatex",
        "command": "pdflatex",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "%DOC%"
        ]
    },
    {
        "name": "bibtex",
        "command": "bibtex",
        "args": ["%DOCFILE%"],
        "env": {}
        },
    {
        "name": "makeglossaries",
        "command": "makeglossaries",
        "args": [
            "%DOCFILE%"
        ]
        }
],
"latex-workshop.view.pdf.viewer": "tab",
````

Now you can simply clone this Repository and open the `main.tex` File. When you press Save you automatically should get a preview of the generated pdf file and autoreloading upon changing the content.

## TODO
- Perhaps elaborate on the Gestaltprinzipien (other principles as well)
- Perhaps discuss Analysis of data in theory (via Jupyter Notebook etc.)