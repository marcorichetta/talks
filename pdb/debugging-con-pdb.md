---
theme: night
highlightTheme: "base16/dracula"
enableMenu: true
controlsTutorial: false
transition: slide
logoImg: "qwe.webp"
title: "Debugging con Pdb"
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

::: right
<img alt="Foto de perfil" loading="lazy" style="border-radius: 999px;" src="pycamp.jpg">
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

--

<!-- .slide: data-background-iframe="https://www.youtube.com/embed/tpIctyqH29Q" -->

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
