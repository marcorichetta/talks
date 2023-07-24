---
theme: night
highlightTheme: "base16/dracula"
enableMenu: false
controlsTutorial: false
transition: slide
logoImg: "meli.jpg"
title: "Debugging con Pdb"
exportHTMLPath: ../export
width: 1920
height: 1080
---

# Pdb

<small>o como encontrar errores sin print()</small>

note: En esta charla veremos qué es `pdb`, qué funcionalidades nos brinda y como usarlo en nuestro día a día, tanto desde
un IDLE, una terminal hasta utilizándolo mediante la GUI de VSCode. También veremos como usarlo en nuestros tests

---

## Dr Who?

::: .container

::: left

-   Córdoba 🇦🇷
-   Trabajando en mejorar la DX de Python @ Code Eco
    -   Python
    -   Poetry
    -   and beyond ?)

:::

:::

---

1. Debugging, why?
2. pdb
3. Demo 🔥

note: primero un poco de historia,
despues vemos las features de pdb y
por ultimo una demo de como usar esto localmente, con apps web o hasta en un lab

---

### Por qué hablamos de _"Debugging"_?

note: Qué tiene que ver un insecto con un error de computación?
En parte se lo debemos a Grace Hopper y su equipo.

--

Esta polilla

![alt](https://upload.wikimedia.org/wikipedia/commons/thumb/f/ff/First_Computer_Bug%2C_1945.jpg/971px-First_Computer_Bug%2C_1945.jpg)

note: Documentaron en 1945 el primer bug atrapado en una computadora (literal)

--

![ENIAC](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Eniac.jpg/1005px-Eniac.jpg)

<figcaption>ENIAC, una de las primeras computadoras de propósito general</figcaption>

--

<!-- .slide: data-background-iframe="https://www.youtube.com/embed/tpIctyqH29Q" -->

---

## Python Debugger

::: {.grid style="--cols-xl: 2;"}

-   Introducido en 1992 [2 años después de Python](https://github.com/python/cpython/commit/921c82401b6053ae7dacad5ef9a4bd02bdf8dbf1#diff-98d47941a1bfadcfdfe02973122c83be2940ca6f3b1c32ca8898e7f594d2669d)

-   Parar tu programa en un punto determinado
-   Inspeccionar variables, source code, ejecutar expresiones

![PDB birth](pdb.png)

:::

---

## Demo time 🔥

---

### Versiones soportadas

```yaml
labs:
    jupyter:
        version: "1" # 1.2.6
        version: "2" # 2.3.2
        version: "3" # 3.2.9
```

<small>Docs: https://furydocs.io/mlp-config/0.3.4/guide/#/schemas/labs/schema </small>
