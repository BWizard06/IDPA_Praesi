<template>
    <div class="slidev-layout relative h-full w-full">
      <!-- Header -->
      <header class="absolute top-0 text-xs left-0 right-0 p-2 flex justify-between items-center">
        <div class="names">{{ $slidev.configs.author || 'Author Name' }}</div>
        <div class="date">{{ new Date().toLocaleDateString() }}</div>
      </header>
  
      <!-- Title -->
      <div class="mt-12 mb-4">
        <slot name="title"/>
      </div>
  
      <!-- Main content with code and diagram side by side -->
      <div class="grid grid-cols-2 gap-4 h-[calc(100%-8rem)]">
        <div class="overflow-auto">
          <slot name="code"/>
        </div>
        <div class="overflow-auto flex flex-col justify-center">
          <slot name="diagram"/>
        </div>
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