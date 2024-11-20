---
# You can also start simply with 'default'
theme: academic
colorSchema: light
themeConfig: 
  paginationY: 'b'
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: KSH-Unterrichtsplaner
author: Ben Brändle | Shahin Amon | Lambotharan Logendran
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: view-transition
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# take snapshot for each slide in the overview
overviewSnapshots: true
hideInToc: true
---

# KSH-Unterrichtsplanung
## Interdisziplinäre Projektarbeit

---
transition: view-transition
layout: 'title-content'
hideInToc: true
---
<template v-slot:title>

# Inhaltsverzeichnis
</template>

<template v-slot:content>
<v-clicks>

<toc />

</v-clicks>
</template>

---
transition: view-transition
layout: 'title-content'
---

<template v-slot:title>

# Aufgabenstellung

</template>

<template v-slot:content>

<v-clicks depth="2">

  - Kalender 
  - Lehrkräfte
    - Ansicht
    - Lektionen erfassen und bearbeiten 
    - Hausaufgaben
    - Prüfungen
    - Notizen
  - Sus
    - Kalendaransicht 
  - Importieren 

</v-clicks>
</template>


---
transition: view-transition
layout: 'two-content'
---

<template v-slot:title>

# Planungsinstrumente
</template>

<template v-slot:left>

  ## Projektmanagements-Methode
</template>

<template v-slot:right>

  ## Kollaborationssoftware / Groupware
  
</template>

---
transition: view-transition
layout: two-content
---

<template v-slot:title>

# Zeitplanung
</template>

---
transition: view-transition
layout: title-content
---

<template v-slot:title>

# Backend
</template>

<template v-slot:content>

> Alles was der User nicht sieht
<div class="mt-4">
  <v-clicks at="2">
  - Technologieauswahl und Vergleiche
  </v-clicks>
</div>
</template>

---
transition: view-transition
layout: section
---

<template v-slot:title>

# Demo
</template>

---
transition: view-transition
layout: section
---

<template v-slot:title>

# Fazit 
</template>
