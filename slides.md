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
record: dev
download: true
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
zoom: 1.1
---

# About Me


- Córdoba 🇦🇷 
- Living in Copenhagen 🇩🇰
- Making the world a better place™ with software since ~2016
- I like to play bass and I'm a dog owner (I miss you so much Lola 🐶)


---

# Slides

<img src="/github-qr.webp" alt="Github QR code" class="w-80">

## https://marcorichetta.github.io/talks/1


---
layout: two-cols
---

# Agenda

<div v-click>

- Why translate?
- Py-Docs-ES story 🇪🇸
- What you can do?

</div>

::right::

# Goals

<div v-click>

- Make you aware of the **importance of translation**.
- Inspire you to **contribute to existing initiatives** (🇵🇹 🇵🇱 🇹🇷 🇰🇷 + 8).
- Promote it in **your own language**!

</div>

<div
  v-motion v-click
  :initial="{ x: -30 }"
  :enter="{ x: 325, y: -48 }"
  :click="{ x: 30 }"
  :leave="{ x: 1000 }"
>
  🇨🇿 anyone?
</div>

<!--
[click] ### Agenda
- I’m here to tell you about our journey with the Python translation to Spanish.
- And for that, the agenda will cover
- First why I think it's important to translate the documentation.
- Then share our experience with the Spanish translation: how we started, and what we have achieved
- Finally, I will tell you what you can do to start contributing

[click] ### Goals

As for the goals, I have **3** for this talk

[click] Czech anyone?
If at least one person feels inspired to contribute, I will feel accomplished 😁
-->

---
layout: center
---

# How many of you do not speak English natively? 🖐️

<!--
Just to check if you are awake

How many of you don not speak English natively?

Could you raise your hand?

Optional: Ok, nice distribution
-->

---
layout: section
---

# Why Translate?

<!--
- Documentation is crucial for the development and growth of any project.
- I mean, we work in i18n because of our users.
- Why not do it for Python itself?
-->

---

## Internet users by language - March 2020

<div class="flex justify-center mb-4">
    <img src="/internet_users_2025.jpg" alt="Internet users by language" width="600">
    <div class="absolute bottom-5 right-60 text-gray-500">
        Source: <a href="https://en.wikipedia.org/wiki/Languages_used_on_the_Internet#Internet_users_by_language">Wikipedia</a>
    </div>
</div>

<!--
- It turns out 75% of the internet users **don't speak English** as their first language
- (Optional) As we saw when raising hands
-->

---

## Top 10 million websites by language content - March 2025

<div class="flex justify-center mb-4">
    <img src="/language_usage_2025.jpg" alt="Language usage by website" width="550">
    <div class="absolute bottom-5 right-60 text text-gray-500">
        Source: <a href="https://en.wikipedia.org/wiki/Languages_used_on_the_Internet#Internet_users_by_language">Wikipedia</a>
    </div>
</div>

<!--
- 50% of the websites are in English
-->

---
layout: statement
---

# There is a need for translation

<!--     
- Documentation is crucial for the development and growth of any project.
- I mean, we work in i18n because of our users.
- Why not do it for Python itself?
-->


---
layout: quote
---

# "_Having the docs in our language means people can feel like home_" 🏡
Cristián Maureira

<!--
I want to paraphrase Cristián Maureira, who is also part of the project

Read phrase

I think you can relate to this feeling, specially if you live abroad and see something in your native language.

It grabs your attention immediately.
-->

---

# Useful for

<v-clicks>

- **New Users** -> official content to learn Python
- **Educators and Newcomers** -> teaching programming in native language
- **Getting started in open source** -> first contribution experience
- **Other Contributors** -> inspiration from other translations

</v-clicks>

<!--
This is also useful because of other reasons:

<v-clicks>

- **New Python Users**: can benefit from an official structured path to learn Python.
- **Educators and Newcomers**: Programming is being taught at younger ages. Being able to teach it to young people in their native language is a big plus.
- **Contributing to Open Source**:  It's a great way to get started in open source.
- **Other Contributors**: I took a lot of inspiration from the 🇵🇹 translation when helping on the 🇪🇸 one
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
- This is a snapshot of it in December 2019 (Thanks Wayback Machine, amazing piece of software)
- People who didn't have good English had to rely on translation services or community content
- Which are fine most of the time, but not always specially for reference material
-->

---
transition: slide-up
---

# May 2019
- Marian Vignau 🇦🇷 assisted Pycon US
- Finds out Raúl Cumplido 🇪🇸 was working on the Spanish translation.
- Inspired by the 🇫🇷 translation

<v-click>
<div
    v-motion
    :initial="{ opacity: 0, scale: 0.8 }"
    :enter="{ opacity: 1, scale: 1, transition: { duration: 1000 } }"
>
    <h1 class="text-center p-10">
        Community 🫶
    </h1>
</div>
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

# April 2020


<div class="flex justify-center items-center">
    <img src="/Vinicius.png" alt="Vinicius Ferreira" class="absolute top-50 border-1 rounded-lg">
    <div class="absolute bottom-25 text-gray-500">
        Vinicius Ferreira 🇧🇷 talked about the 🇵🇹 translation in Python Pizza Remote.
    </div>
</div>

<!--
Then Vinicius Ferreira 🇧🇷

Which led to other spanish speakers 
who were listening to do the same.

-->

---
transition: slide-up
layout: center
---


![alt text](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExb3o1ZDFva2pkaTRtcTh0YnBsdDVqbWdxc3Y4eGZudHFuMjBobjY5aSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/DoWqmz4TGL3Tk9jwTZ/giphy.gif)

<!-- The magic of the Internet happened -->

---
transition: slide-up
---

<div class="flex justify-center">
  <img src="/collaboration.png" alt="Discourse collaboration" width="800" border="1">
</div>
<div class="text-center text-gray-500">Marian telling about the work they were doing with Raúl, in the Python 🇦🇷 forum</div>

<!--
and made interested people find each other and join efforts.

This is Marian telling about the work they were doing with Raúl, in the Python Argentina forum

A month later, we had a group of people interested in translating the docs to Spanish.
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
transition: slide-up
layout: center
---

<div class="flex justify-center">
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3JscnA4ZGJha3lpcGZkbnpub3ZoNWh5bXBxcnl3NHgxZGZ4MngwbiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/aNqEFrYVnsS52/giphy.gif" alt="Cat gif" width="700">
</div>

<!--
A month later
- lots of messages on telegram
- and lots of pull requests
-->

---
transition: slide-left
---

# **June 2020**

https://docs.python.org/es was a reality! 🚀

<div class="flex justify-center">
  <img src="/docs-translation.png" alt="First screenshot of the translated docs" width="800">
</div>

<!--
## We were part of the official docs!
-->

---

<div class="grid grid-cols-[2fr_4fr] gap-4">
    <div>
        <h1>Some numbers</h1>
        <div class="mt-4">
                <p><strong>+4300</strong> commits</p>
                <p><strong>350</strong> files translated (> 75%)</p>
                <p><strong>+250</strong> contributors (and counting)</p>
        </div>
    </div>
    <div class="flex items-center justify-center">
        <img src="/contributors.png" alt="Contributors" width="100%" />
    </div>
</div>

<!--
These are some of the numbers so far.
-->

---
layout: section
---

# What can you do?

<!--
I talked about Why translate and shared our story.

but What can you do?
-->

---
layout: two-cols
---

# Ask for help 🫂
<br>

## ContributGuide 
https://python-docs-es.readthedocs.io/es/3.13/CONTRIBUTING.html


## Telegram channel:
https://t.me/python_docs_es

::right::

<div class="flex justify-center">
    <img src="/qr_telegram.jpg" alt="Telegram QR code">
</div>

<!--
First of all, don't forget you always can ask for help on how to get started
or just to say hi!

We have a guide with the required step-by-step configuration to get started
-->

---
layout: two-cols
---

# Our Process

- Fork the main repository
- Request a file to translate
- Translate it on your computer
- Commit, push and create the pull request
- Wait for feedback from a reviewer
- Success 🎉

::right::

<div class="flex justify-center" v-click>
    <img src="/issues-PRs.png" alt="Translation process" width="100%">
</div>

<!--
1. Leer el process

[click] And, as you can see, there are many pages waiting to be translated
-->

---

# Contributing to Python doesn’t have to be scary!

![](/python-issues-github.png)

<!--
Usually this is what we imagine when we say "contribute to Python"

But it's not only way, in fact
-->

---

# http://devguide.python.org/#contributing

<div class="flex items-center justify-center">
    <img src="/python-docs-contributing.png" alt="Contributing guide" width="100%" />
</div>

<Arrow x1="600" y1="340" x2="515" y2="340" color="red" v-click />

<!--
Making this talk I discovered this page.

I think it's great because it shows many ways to contribute depending on the role you have.

[click] I noticed translating doesn't have a guide (yet)

Another nice opportunity to standardize this process across communities
-->

---
layout: statement
---

# Extra

---

# A word about LLMs 🤖

<v-clicks>

- What role do LLMs play in this?
- Will they replace us in translation?

</v-clicks>

<!-- 
This wouldn't be a 2025 talk if there's no AI in it

**You may ask**

- What role do LLMs play in this?
- We cannot ignore that they're pretty useful in translation.

In fact, GPT-1, the ancestor of Chatgpt, did a very good job at it.

but
-->

---
zoom: 0.8
---

<div class="grid grid-cols-2 gap-4">
    <div>
        <h1>"Craftsmanship as resistance to performance"</h1>
    </div>
    <div class="flex justify-center items-center">
        <img src="/burnout.jpg" alt="The burnout society" width="80%">
    </div>
</div>


<!--
I'm bringing up Byung Chul Han, philosopher, who in his book, Burnout Society, talks about

craftsmanship as resistance to performance, where everything must be fast, useful, and quantifiable.


Whether you agree with this opinion or not,
-->

---

# Closing Thoughts


<v-clicks>

- It’s not only translation; it's a great opportunity to **learn**

- Getting started in  **Open Source**

- It's a way of giving back to the **community**

</v-clicks>

<!--
- Translation is just a part of the process
- it's an excellent opportunity to **Learn** (about Python and how to work in a group)

- Getting started in Open Source

- Giving back to the **community**,
  - you never know the people you get to know when helping others.

And most importantly,
-->

---
layout: intro-image
image: https://live.staticflickr.com/65535/53938930235_3921adef78_3k.jpg
---

<div class="text-center bg-sky-600 bg-opacity-50 px-2 mx-8 rounded-lg">
  <h1>Be part of something bigger</h1>
</div>

<!--
It let's you be part of something bigger 

how the python community
-->

---
layout: two-cols
---

# Thank You!

<div class="flex justify-center">
    <img src="/ciao-gif.webp" alt="Ciao animation" class="h-64 my-auto">
</div>

<div class="absolute left-33 bottom-40 text-gray-400">
    Illustration by Matteo Giuseppe Pani
</div>

<div class="absolute bottom-10">
    <span class="font-600">
        How to Contribute to the Python Community in Your Own Language
        <br>
        @marcorichetta - EuroPython 2025
    </span>
</div>

::right::

# Let's connect!

Currently looking for a job
<img src="/linkedin-qr.webp" alt="LinkedIn QR code" class="w-80">
