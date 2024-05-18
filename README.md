
<p align="center">
  <img src="attachments/python-flask.png" alt="image" z>
</p>


<div align="center">
  <h1>PROJECTE M04 Javier González Sánchez</h1>
</div>


El projecte consisteix en *desenvolupar una aplicació* amb **python** + **flask** que mostra el contingut de **XMLs** en format **feed**/**rss** maquetat amb **bootstrap**.

## PIP. Que és?

Et permet **instal·lar i administrar** paquets de programari escrits en *Python* que estan disponibles al *Python Package Index (PyPI)*. *PyPI* és un **repositori de programari** per a la comunitat de *Python*, que conté milers de paquets que poden ser instal·lats i utilitzats en projectes de *Python*.

Mes informació [aqui](https://docs.python.org/es/3.8/distutils/packageindex.html).

## Entorns virtuals

Els **entorns virtuals** són una manera de crear i gestionar un entorn d'execució aïllat per a les teves aplicacions. Això facilita el desenvolupament de projectes ja que manté les dependències separades i evita conflictes amb l'entorn global del sistema. Amb *Python*, el mòdul **venv** et permet crear entorns virtuals.

Mes informació [aqui](https://docs.python.org/es/3/library/venv.html)

## Flask

Flask és un marc de treball web lleuger i flexible per a Python que facilita la creació d'aplicacions web. És conegut per la seva simplicitat i facilitat d'ús. El seu enfocament minimalista el fa una excel·lent opció tant per a principiants com per a desenvolupadors experimentats.

Mes informació [aqui](https://www.ionos.es/digitalguide/paginas-web/desarrollo-web/flask/).

## Feedparser

Feedparser és un mòdul de Python que permet analitzar feeds RSS i Atom. Amb Feedparser, pots extreure informació de feeds de notícies, blogs, podcasts, etc. d'una manera senzilla i eficient.

Mes informació [aqui](https://github.com/kurtmckee/feedparser)


## Instalació entorn virtual

Per instalar i crear l'entorn virtual necessitarem:

**Per començar:**

1. Crearem una carpeta amb el nom del projecte.
2. Descarreguem o obrim *Visual Studio Code* si ja el tenim
3. Obrim la carpeta a la terminal

<p align="center">
  <img src="attachments/captura_carpeta.png" alt="image" width="650" height="200">
</p>


4. Descarreguem l'entorn virtual amb: `python3 -m venv .venv`
5. Activem l'entorn virtual:
- *Linux* : `source .venv/bin/activate`
- *Windows* : `.venv\Scripts\activate`
6. Un cop activa, ja podem instalar *Flask* i el *Feedparser*:
- `pip install flask`
- `pip install feedparser`
7. Crearem un fitxer *Python* de nom **app.py**, que sera fill de la carpeta arrel. Més endavant utilitzarem aquest fitxer.

<p align="center">
  <img src="attachments/crear-app-py.png" alt="image">
</p>

Per facilitar la integració entre el *Visual Studio Code* i l'entorn virtual descarreguem l'extensio:

[Python Environment Manager](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-environment-manager)

Amb aixo ja tenim el entorn virtual instalat i configurat.

**Tutorial**

https://youtu.be/W2LCF3YYpIY?feature=shared

**Mes info**

https://gee.es/2023/05/17/como-creo-un-entorno-de-desarrollo-con-env-en-vscode/

## Funcionament Flask

### Hello world

1. Primer de tot, initzialitzarem amb : `flask run --debug`
2. Crearem un fitxer **index.html**

```
<!DOCTYPE html>
<html lang="ca">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello World amb Flask i Jinja</title>
</head>
<body>
    <h1>Hello World!</h1>
    <p>Exemple de página web estática amb Flask i Jinja.</p>
</body>
</html>
```
3. Afegim la ruta al nostre fitxer **app.py**

```
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')
```

4. Obrim al nostre navegador la *url* http://127.0.0.1:5000/, i si tot esta bé aquest será el resultat.

<p align="center">
  <img src="attachments/html.png" alt="image">
</p>

### Funcionament per local o per remot

Al nostre codi bàsic, al fitxer **app.py**, tenim una funció que permet executar l'arxiu *RSS* al mode local o al mode remot.

**Mode remot**: Per tractar les dades desde la web directament comenten la linea que tracta les dades desde la local

<p align="center">
  <img src="attachments/remot.png" alt="image">
</p>

**Mode loca**: A la inversa, comenten la linea que tracta les dades desde mode remot.

<p align="center">
  <img src="attachments/local.png" alt="image">
</p>












<p>&nbsp;</p>
