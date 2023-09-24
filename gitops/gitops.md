---
theme: sky
highlightTheme: "base16/dracula"
enableMenu: false
controlsTutorial: false
transition: slide
logoImg: "nerd-square-detailed.png"
title: "Intro a GitOps con Flux"
---

## Intro a GitOps con Flux

Marco Richetta - Nerdearla 2023

---

## About me

-   Las Perdices, Córdoba 🇦🇷
-   Python DX @ Mercado Libre
-   @marcorichetta

---

## Agenda

1. GitOps
1. Flux
1. Demo
1. Recap

note: En esta charla vamos a ver qué es GitOps,
por qué surge y que ventajas trae.
Seguido de eso les voy a contar sobre Flux, un set de herramientas para implementar GitOps.
Finalmente haré una demo con Flux para que veamos su funcionamiento step by step.

---

### Objetivo

1. Que conozcan de que va gitops
2. Que aprendan sobre flux
3. Que lo puedan probar localmente

--

A quién va dirigida?

-   Usas `kubectl apply` desde tu compu o CI
-   Querés automatizar deployment de infraestructura
-   Buscas una alternativa/complemento a Terraform (Crossplane FTW)
-   **Nerds**, obvio

---

## YAOps

Yet Another \*Ops

--

![gitops-fever](image.png)

note: No nos dejemos llevar por _the new kid on the block_
Para mí, lo valioso de estas tecnologías es la variedad que existe.
Adaptemoslas a nuestro uso. Al final todo termina siendo `ClickOps`

---

## GitOps Timeline

--

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

--
