---
theme: night
highlightTheme: "base16/dracula"
enableMenu: false
controlsTutorial: false
transition: slide
title: "Debugging con Pdb"
width: 1200
height: 900
totalTime: 1200
---

# Pdb

<!-- .slide: data-timing=30 data-background="bug.jpg" -->

<small>o como encontrar errores sin print()\*</small>

note: Photo by Skyler Ewing: https://www.pexels.com/photo/harmonia-axyridis-ladybug-on-green-leaf-6313159/

---

<!-- .slide: data-timing=30 -->

## Who?

-   Marco Richetta
-   Córdoba 🇦🇷
-   Python DX @ Mercado Libre

note: Soy de Cordoba, por si no se nota la tonada. Trabajo en Code Eco entre otras cosas en mejorar la DX de Python

---

<!-- .slide: data-timing=45 -->

## Agenda

1. pdb
1. Demo 🔥
1. Recursos extra

note:
Una intro al debugging <br/>
despues pasamos pdb y sus funcionalidades <br/>
una demo de como usarlo en scripts, notebooks de Jupyter (lo que usamos en labs) <br/>
por último tips y algunos recursos extra

---

### Por qué hablamos de _"Debugging"_?

note: Qué tiene que ver un bug o insecto con un error de computación?
En parte se lo debemos a una polilla.

--

![Domino meme](domino.png)

--

![alt](https://upload.wikimedia.org/wikipedia/commons/thumb/f/ff/First_Computer_Bug%2C_1945.jpg/971px-First_Computer_Bug%2C_1945.jpg)

_Bug_ capturado en la Harvard Mark II, Septiembre 1947

note: El primer bug (literal) documentado que rompió un programa

--

![ENIAC](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Eniac.jpg/1005px-Eniac.jpg)

ENIAC, una de las primeras computadoras de propósito general

note: Computadoras del tamaño de habitaciones, con componentes electromecánicos

--

<!-- .slide: data-background="crashcourse.jpg" -->

<!-- <iframe class="stretch" data-src="https://www.youtube.com/embed/tpIctyqH29Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->

note: Si les interesa conocer datos como este u otros aprovecho a recomendarles este curso
sobre la historia de la computación

---

## Python Debugger

![PDB birth](pdb.png)

Introducido en 1992 ([2 años después de Python](https://github.com/python/cpython/commit/921c82401b6053ae7dacad5ef9a4bd02bdf8dbf1#diff-98d47941a1bfadcfdfe02973122c83be2940ca6f3b1c32ca8898e7f594d2669d))

note: No es algo nuevo, ya tiene la mayoría de edad

--

#### Controlar la ejecución de tu programa

-   Inspeccionar variables
-   Ejecutar expresiones
-   Explorar el código

```python
# Shell
python -m pdb script.py

# Python +3.7
breakpoint()

# Retrocompatible
import pdb; pdb.set_trace()
```

note: Esta funcionalidad aplica a cualquier debugger, no solo al de Python. **IMPORTANTE**

--

### Comandos más comunes

-   `p (rint)` - inspeccionar una variable
-   `l (ist)` - mostrar el código del programa
-   `c (ontinue)` - continuar la ejecución del programa
-   `n (ext)` - cotinuar la ejecución hasta la siguiente línea
-   `j (ump)` - setea la próxima linea a ser ejecutada
-   `h (elp)` - mostrar comandos disponibles y docs

note: 5/6 minutos

---

<!-- .slide: data-timing=540 -->

## Demo time 🔥

note:
python -m pdb <br/>
demo.py <br/>
pip install ipdb <br/>
notebook <br/>
UI

---

## Tips

#### Podes deshabilitar los breakpoint

```python
PYTHONBREAKPOINT=0 python demo.py
```

<br>

#### Pero si te olvidas... 🚧 {class="fragment"}

pre-commit hook: [`debug-statements`](https://pre-commit.com/hooks.html) {class="fragment"}

note: Chequea pdb statements en tu código

--

#### Pytest ❤️ Pdb (_`ipdb` compliant_)

```python
pytest --pdb
```

<small>Docs: https://docs.pytest.org/en/latest/how-to/failures.html#using-python-library-pdb-with-pytest</small>

--

## Recursos

-   [ipdb](https://github.com/gotcha/ipdb)
-   [pdb++](https://github.com/pdbpp/pdbpp)
-   [VSCode debugging](https://code.visualstudio.com/docs/python/debugging)
-   [Pycharm debugging](https://www.jetbrains.com/help/pycharm/debugging-your-first-python-application.html)
-   [Pystack](https://github.com/bloomberg/pystack)

note: pdb con esteroides
Inspeccionar procesos de Python en ejecución o core dumps para entender que se ejecuta/ó

--

Cheatsheet

![PDB cheatsheet](cheatsheet.png)
https://www.nnja.io/2019/python-debugging-cheatsheet.pdf

---

![@giphy](https://media.giphy.com/media/KJ1f5iTl4Oo7u/giphy.gif)
