---
title: "Intro a GitOps con Flux"
author: Marco Richetta
theme: robot-lung-ebi
customTheme: "css/override"
highlightTheme: "base16/dracula"
controls: false
controlsTutorial: false
enableMenu: false
progress: false
transition: slide
logoImg: "nerd-logo.png"
width: 1440
height: 900
totalTime: 1200
---

<!-- .slide: data-background="https://github.com/sysarmy/2023.nerdear.la/blob/main/app/static/img/hero-background.jpeg?raw=true" data-background-transition="zoom" -->

# Intro a GitOps con Flux {style=color:white;font-style:italic}

<h4 style="color:white;font-family:Roboto">
Marco Richetta

Nerdearla 2023

</h4>

---

<!-- .slide: data-timing=90 data-background-transition="zoom" -->

## About me

::: .container

::: left

-   Las Perdices, Córdoba 🇦🇷
-   Aprendiendo de software desde 2016
-   Haciendo cosas @ Mercado Libre
-   [marcorichetta.dev](https://www.marcorichetta.dev/)

:::

::: right

![Lola](lola.jpg){height=600, style="border:0"}

:::

:::

---

<!-- .slide: data-timing=60 -->

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

<!-- .slide: data-timing=120 -->

## Objetivo

1. Que conozcan de que va gitops
2. Que aprendan sobre flux
3. Que lo puedan probar localmente

--

## A quién va dirigida?

-   Usas `kubectl apply` desde tu compu o CI
-   Querés automatizar deploys de apps/infra
-   Buscas una alternativa/complemento a Terraform
-   **Nerds**, obvio

---

<!-- .slide: data-timing=180 -->

# YA\*Ops

(Yet Another \*Ops)

--

![ops fever](ops-fever.png){height=900}

note: No nos dejemos llevar por _the new kid on the block_.
Para mí, lo valioso de estas metodologías es la variedad.
Al igual que con nuevas tecnologías, tenemos que saber adaptarlas a nuestro uso.
Al final todo termina siendo `ClickOps`

--

![clickops](clickops.png){height=300}

---

<!-- .slide: data-timing=45 -->

# GitOps

![Flow](flow.png)

note:
Es un modelo de trabajo basado en Git como **source of truth.** <br>
Git no solo para código de apps<br>
sino también para crear, modificar y eliminar recursos.<br>
Es una forma de implementar IaC

---

### Timeline

<!-- .slide: data-timing=180 -->

![timeline](gitops-timeline.png){width=1200}

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

--

![Flux General availability](flux-ga.png)

note: 10 MINUTOS

---

<!-- .slide: data-background-image="principles.png" data-background-size=1400px -->

---

# Push vs Pull Based Deployments

--

## Push

![Push Based deploy](push-deploy.png)

-   Approach tradicional (GH Actions, Gitlab CI, Jenkins)
-   Deployment Pipeline contiene credenciales (⚠️ God mode ⚠️)
-   No detecta desvíos entre el Environment Repo vs Environment

--

## Pull

![Pull Based Deploy](pull-deploy.png)

-   _Deployment Pipeline_ => _Operator_
-   Encargado de observar y comparar continuamente el **estado deseado** vs el **estado actual**

-   Permisos sync con k8s (RBAC)

-   Además monitorea el _Image Registry_ para encontrar nuevas versiones de imágenes

note:
Cuando el `Environment` cambie de cualquier manera que no esté descrita en nuestro `Environment Repository`, **estos cambios serán revertidos**. <br>
Asegura que **todos los cambios en nuestro `Environment` deben pasar por git** <br>
También se puede sincronizar manualmente 🙌

---

![flux-logo](flux.png){width=1200, style="border:none";}

> Flux is a set of continuous and progressive delivery solutions for Kubernetes

--

## Features

::: .container

::: left

**Git push y Flux se encarga del resto**

:::

::: middle

**Flux 🤝 Tools**

<ul>
<li><b>Git providers</b>: Github, Gitlab, Bitbucket, hasta S3!</li>
<li><b>Container registries</b></li>
<li><b>K8s:</b>: Kustomize, Helm, RBAC</li>
</ul>

:::

::: right

**Monitoreo**

<ul>
<li><b>Health checks</b></li>
<li><b>Alertas</b>: Grafana, Datadog</li>
<li><b>Notificaciones</b>: Github, Slack, Discord</li>
</ul>

:::

:::

--

## Controllers

En Kubernetes, los Controllers ejecutan _control loops_ que observan el **estado del cluster** y solicitan o ejecutan cambios según se necesite, con el objetivo de llegar al **estado deseado.**

![Flux controllers](controllers.png)

note: Ej: termostato

--

## ![Flux Diagram](flux-diagram.png)

note:
Source: Sincroniza los sources (Git, Bucket, S3) y los guarda como artefactos para ser utilizados por otros ctrls.<br>
Kustomize: Genera, valida y aplica los manifiestos en el cluster.<br>
Helm: Manejo de Helm Releases y Charts.<br>
Notification:<br>
Notifica a nuestro sistema de eventos externos (Github, Gitlab, Docker)<br>
Notifica a sistemas externos (Slack, Discord, Teams) de nuestros eventos<br>
Image Reflector: Escanea repos de imagenes (Docker, OCI) y guarda la image metadata para ser usada por el **Automation Controller** 👇<br>
Automation: Actualiza archivos YAML (`git commit`) cuando nuevas imagenes están disponibles. ⇒ **Kustomize Controller** nota el cambio y empieza a sincronizar<br>

---

<!-- .slide: data-background-image="https://media.makeameme.org/created/aaaaand-demo-time.jpg" -->
