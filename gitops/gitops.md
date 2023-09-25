---
theme: robot-lung-ebi
highlightTheme: "base16/dracula"
controls: false
controlsTutorial: false
transition: fade
logoImg: "nerd-logo.png"
title: "Intro a GitOps con Flux"
width: 1440
height: 900
totalTime: 1200
---

<!-- .slide: data-timing=30 data-background="https://github.com/sysarmy/2023.nerdear.la/blob/main/app/static/img/hero-background.jpeg?raw=true" data-background-transition="zoom" -->

# Intro a GitOps con Flux {style=color:white;font-style:italic}

<h4 style="color:white;font-family:Roboto">
Marco Richetta

Nerdearla 2023

</h4>

---

<!-- .slide: data-timing=30 data-background-transition="zoom" -->

## About me

-   Las Perdices, Córdoba 🇦🇷
-   Python DX @ Mercado Libre
-   @marcorichetta

---

## Agenda

1. Intro
1. GitOps
1. Flux
1. Demo
1. Recap

note: En esta charla vamos a ver qué es GitOps,
por qué surge y que ventajas trae.
Seguido de eso les voy a contar sobre Flux, un set de herramientas para implementar GitOps.
Finalmente haremos una demo para ver su funcionamiento paso a paso.

---

## Objetivo

1. Que conozcan de que va gitops
2. Que aprendan sobre flux
3. Que lo puedan probar localmente

--

## A quién va dirigida?

-   Usas `kubectl apply` desde tu compu o CI
-   Querés automatizar deploys de apps/infra
-   Buscas una alternativa/complemento a Terraform (Crossplane FTW)
-   **Nerds**, obvio

---

# YA\*Ops

(Yet Another \*Ops)

--

<img src="ops-fever.png" height=800>

note: No nos dejemos llevar por _the new kid on the block_.
Para mí, lo valioso de estas metodologías es la variedad.
Al igual que con nuevas tecnologías, tenemos que saber adaptarlas a nuestro uso.
Al final todo termina siendo `ClickOps`

--

<img src="clickops.png" height=300>

---

# GitOps

![Flow](flow.png)

note:
Es un modelo de trabajo basado en Git como **source of truth.** <br>
Mix entre DevOps e IaC <br>
Git para creamos, modificamos y eliminamos nuestros recursos.

---

## Timeline

![timeline](gitops-timeline.png)

note:
2017 - _GitOps_ es acuñado por primera vez por Alexis Richardson<br>
2018 - Empieza a ganar tracción.<br>
Referentes hablan<br>
Cloud providers importantes lo adoptan<br>
También se crea ArgoCD<br>
2019 - Flux es aceptado en la CNCF Sandbox<br>
2020 - CNCF adoption de Flux<br>
1st GitOpsDays conf<br>
2021 - 1st GitOpsCon<br>
Se crea OpenGitOps para acelerar la adopción<br>
2022 - Flux y ArgoCD se graduan

---

<!-- .slide: data-background-image="principles.png" data-background-size=1400px -->

---

# Push vs Pull Based Deployments

--

## Push

![Push Based deploy](push-deploy.png)

-   Approach tradicional (GH Actions, Gitlab CI, Jenkins)
-   Deployment Pipeline contiene credenciales
-   No deteca desvíos entre el Environment Repo vs Environment

--

## Pull

![Pull Based Deploy](pull-deploy.png)

-   _Deployment Pipeline_ => _Operator_
-   Encargado de observar y comparar continuamente el **estado deseado** vs el **estado actual**

-   Además monitorea el _Image Registry_ para encontrar nuevas versiones de imágenes

-   También se puede sincronizar manualmente 🙌

note:
Cuando el `Environment` cambie de cualquier manera que no esté descrita en nuestro `Environment Repository`, **estos cambios serán revertidos**. <br> Asegura que **todos los cambios en nuestro `Environment` deben pasar por git**
