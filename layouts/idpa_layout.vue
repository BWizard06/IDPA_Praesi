<template>
    <div class="layout-base">
      <!-- Main content slot -->
      <slot />
  
      <!-- Footer with name, date, and page number -->
      <footer class="footer">
        <div class="footer-content">
          <span>{{ name }}</span> |
          <span>{{ date }}</span> |
          <span>Page {{ $page.page }}</span>
        </div>
      </footer>
    </div>
  </template>
  
  <script setup>
  const name = 'Your Name'
  const date = '2024-10-13'  // or you can make it dynamic if you like
  </script>
  
  <style scoped>
  .layout-base {
    display: flex;
    flex-direction: column;
    height: 100%;
  }
  .footer {
    position: absolute;
    bottom: 10px;
    width: 100%;
    text-align: center;
    font-size: 14px;
    color: #666;
  }
  </style>
  