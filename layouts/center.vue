<template>
    <div class="slidev-layout relative h-full w-full">
      <!-- Header -->
      <header class="absolute top-0 text-xs left-0 right-0 p-2 flex justify-between items-center">
        <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
        <div class="date">{{ new Date().toLocaleDateString() }}</div>
      </header>
  
      <!-- Main content centered -->
      <div class="grid h-full place-content-center">
        <slot />
      </div>
  
      <!-- Footer -->
      <footer class="absolute text-xs bottom-0 left-0 right-0 p-2 flex justify-between items-center">
        <div></div>
        <div class="presentation-name text-center">{{ $slidev.configs.title }}</div>
        <div></div>
      </footer>
    </div>
  </template>
  
  <style>
  .slidev-layout {
    @apply px-14 py-10;
  }
  </style>