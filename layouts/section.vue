<template>
    <div class="slidev-layout section-layout relative h-full">
      <!-- Header -->
      <header class="absolute top-0 text-xs left-0 right-0 p-2 flex justify-between items-center">
        <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
        <div class="date">{{ new Date().toLocaleDateString() }}</div>
      </header>
  
      <!-- Section content centered -->
      <div class="section-content text-sm flex items-center justify-center h-[calc(100%-8rem)]">
        <h1 class="text-4xl font-bold"><slot/></h1>
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