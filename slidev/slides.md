---
theme: apple-basic
transition: fade
layout: intro-image-right
image: /enie.png
highlighter: "shiki"
lineNumbers: false
info: |
    ## How to Contribute to the Python Community in Your Own Language
    A talk about translating the official Python documentation into Spanish.
fonts:
    # for product sans
    sans: "Product Sans"
    # for code font
    mono: "Fira Code"

favicon: /favicon.ico
author: Marco Richetta
record: true
drawings:
    presenterOnly: true

defaults:
    # layout: center
    transition: fade
---

# How to Contribute to the Python Community in Your Own Language

#### Translating Python Documentation to 🇪🇸: Experiences and Learnings

<div class="absolute bottom-10">
  <span class="font-600">
    @marcorichetta - EuroPython 2025
  </span>
</div>

<!--
Welcome Everyone! 👋
I'm Marco, and I'm here to talk about how to **contribute to Python in your own language**.

Thanks to EuroPython organizers and volunteers for their help. It’s my first time here and I’m really amazed at the conference size!
-->

---
layout: image-right
image: /about.webp
---

# About Me

<v-clicks>

- Córdoba 🇦🇷 
- Living in Copenhagen 🇩🇰
- Making the world a better place™ with software since ~2016
- I like to play bass and I'm a dog owner (I miss you so much Lola 🐶)
- Looking for a job right now: https://www.linkedin.com/in/marco-richetta/
</v-clicks>

---
layout: center
---

# How many of you do not speak English natively? 🖐️

<!--
Just to check if you are awake
How many...
Could you raise your hand?

Ok, I think this is gonna be more valuable to you.
-->

---

# Goals

<v-clicks>

- Make you aware of the **importance of translation**.
- Inspire you to **contribute to existing initiatives** (🇵🇹 🇵🇱 🇹🇷 🇰🇷).
- Promote it in **your own language**!

</v-clicks>

<div
  v-motion v-click
  :initial="{ x: -30 }"
  :enter="{ x: 285, y: -45 }"
  :click="{ x: 30 }"
  :leave="{ x: 1000 }"
>
  🇨🇿 anyone?
</div>

<!--
I have **three goals** for this talk

// 3 clicks

[click] Czech anyone?

If at least one person feels inspired to contribute to the community, I will feel accomplished!
-->

---

# Agenda

<v-clicks>

- Why translate?
- Py-Docs-ES story 🇪🇸
- What you can do

</v-clicks>

<!--
- I’m here to tell you about our journey with the Python translation to Spanish.
- And for that, the agenda will cover
- First why I think it's important to translate the documentation.
- Then share our experience with the Spanish translation: how we started, and what we have achieved
- Finally, I will tell you what you can do to start contributing
-->

---
layout: section
---

# Why Translate?

<!--
- Documentation is crucial for the development and growth of any project.
- I mean, we work in i18n because of our users.
- Why not do it for Python itself?

- If you know English, you're lucky; most of the knowledge is in that language. But what about people who don't? 😢

We had translation services before
Nowadays it's even easier with LLMs, which I'm gonna mention later in the talk because... 
## AI
-->

---
layout: quote
---

# "Having the docs in our language means people can feel like home 🏡"
Cristián Maureira

<!--
I want to paraphrase Cristián Maureira, who is also part of the project

Read phrase

I think you can relate to this feeling, specially if you live abroad and see something in your native language.

It grabs your attention immediately.
-->

---

# Other reasons

<v-clicks>

- **New Users**
- **Educators and Newcomers**
- **Getting started in open source**
- **Other Contributors**

</v-clicks>

<!--
This is also important because of other reasons:

<v-clicks>

- **New Python Users**: The tutorials provide a structured path to learn Python.
- **Educators and Newcomers**: Programming is being taught at an increasingly younger age. Being able to teach Python to young people in their native language is a big plus.
- **Contributing to Open Source**: This is not directly on translation, but it's a great way to get started in open source.
- **Other Contributors**: I took a lot of inspiration from the 🇵🇹 translation to find more apropiate terms
</v-clicks>
-->

---
layout: section
---

# Our Story: Python-Docs-ES 🇪🇸

<!--
Let's see how we did it
-->

---
transition: slide-up
---

# Back in the day

![Python Docs - Decemeber 2019](/docs-2019.png)

#### <i>Honorable mention to the Wayback Machine</i>

<!--
- the official docs didn't offer a Spanish option
- This is a snapshot of it in December 2019.
- People who didn't have good English had to rely on translation services or community content
- Which are fine most of the time, but not always specially for reference material
-->

---
transition: slide-up
---

# **2019**
- Marian Vignau 🇦🇷 assisted Pycon US
- Finds out Raúl Cumplido 🇪🇸 was working on the Spanish translation.
- Inspired by the 🇫🇷 translation

<v-click>
<h2>Standing on the shoulders of giants</h2>
</v-click>

<!--
- Marian Vignau (🇦🇷) assisted Pycon US
- In a lunch, she finds out Raúl Cumplido (🇪🇸) was working on the Spanish translation.
- Inspired by the (🇫🇷) translation

I included the flags as a way of showing the importance of communities and why not, sharing your work with others
-->

---
transition: slide-up
---

# **April 2020**

Vinicius Ferreira 🇧🇷 talked about the 🇵🇹 translation in Python Pizza Remote.

<!--
Then Vinicius Ferreira 🇧🇷

Which led to other spanish speakers 
who were listening to do the same.

#TODO Agregar contenido
-->

---
transition: slide-up
---


![alt text](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExb3o1ZDFva2pkaTRtcTh0YnBsdDVqbWdxc3Y4eGZudHFuMjBobjY5aSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/DoWqmz4TGL3Tk9jwTZ/giphy.gif)

<!-- The magic of the Internet happened -->

---
transition: slide-up
---

<div class="flex justify-center">
  <img src="/collaboration.png" alt="Discourse collaboration" width="800">
</div>

<!--
and made interested people find each other and join efforts.


This is Marian telling about the work they were doing with Raul.

In the Python Argentina forum
-->

---
transition: slide-up
layout: image-right
image: https://i.giphy.com/h26R1JMxiqYpwp0rkF.webp
---

# **May 1st 2020**

<v-clicks depth="2">

- COVID was making people do all kinds of weird things
- some of us decided to translate the Python docs to Spanish (which is not a weird thing)
- First meeting! 🎉

</v-clicks>

<!--
- COVID was making people do all kinds of weird things
- some of us decided to translate the Python docs to Spanish
    - (which is not a weird thing)
- First meeting!
-->

---
transition: slide-left
---

# **June 2020**

`https://docs.python.org/es` was a reality! 🚀

<div class="flex justify-center">
  <img src="/docs-translation.png" alt="First screenshot of the translated docs" width="800">
</div>

<!--
And a month later
and a lot of messages on telegram

#TODO Gif cat keyboard

## We were part of the official docs
-->

---
layout: image
---

# Some numbers

- **+4300** commits
- **350** files translated (> 75%)
- **+300** contributors (and counting)

![Opened issues and Pull Requests](/issues-PRs.png)

<!--
Grab it while it's hot!
-->

---
layout: section
---

# What you can Do

---

# Contributing to Python doesn’t have to be scary!

![](/python-issues-github.png)

<!--
#TODO Escribir lo que quiero decir
-->

---

![](/python-docs-contributing.png)

<!--
Making this talk I discovered this page.

While it's helpful, it can be daunting for people that want to get started.
-->

---

# Our Process

- Fork the main repository
- Request a file to translate
- Translate it on your computer
- Commit, push and create the pull request
- Wait for feedback
- Success 🎉

#TODO Incluir roles

---

# Ask for help 🫂


## Guide with the required step-by-step configuration:
https://python-docs-es.readthedocs.io/es/3.13/CONTRIBUTING.html

## Telegram channel:
https://t.me/python_docs_es

---

# What About LLMs? 🤖

https://www.gally.net/temp/llms-and-translation/index.html


#TODO Agregar antes una slide que diga EXTRA

Hay un componente en lo artesanal que no queremos perder

<!--
This shouldn't be a 2025 talk if there's no AI in it

- What role do LLMs play in this? 
- We cannot ignore that they're pretty useful in translation.

- Professional translators know that AI will get better and better (99%), and that offers for that 1% you can provide will become scarce.
-->

---

# Closing Thoughts


<v-clicks>

- It’s not only translation; it's a great opportunity to **learn**
- It's a way of giving back to the **community**
- **Get started in Open Source**
- **Contribute to Python**

</v-clicks>

<!--
- Do it for the **community**, you never know the people you get to know when helping others.
- **Learn**: You will learn about Python and how to work collaboratively.
- It’s not only translation; it's a great opportunity to get started on **open source**.
- **Contribute to open source**: It's adding a tiny grain of sand to a collective effort that has been going on for years and will continue beyond us.
-->

---
layout: intro-image
image: https://live.staticflickr.com/65535/53938930235_3921adef78_3k.jpg
---

<div class="absolute top-10 text-center text-3xl">
  <h1>Be part of something bigger than you</h1>
</div>

<!--
But most importantly,

to be part of something bigger than you

Which will trascend us
-->

---
layout: image-right
image: /qr_telegram.jpg
---

# Join us

## https://t.me/python_docs_es

<!--
If you wanna join us or just say hi.
-->

---
layout: intro-image-right
# image: https://media.giphy.com/media/KJ1f5iTl4Oo7u/giphy.gif
image: /ciao-gif.webp
---

# Thank You! 🙏

@marcorichetta - EuroPython 2025

_Illustration by Matteo Giuseppe Pani_
