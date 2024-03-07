<!-- App.vue -->
<template>
    <div id="app">
      <CustomCursor />
      <div class="content">
        <!-- Your main content goes here -->
      </div>
    </div>
  </template>
  
  <script>
  import CustomCursor from './components/CustomCursor.vue';
  
  export default {
    name: 'App',
    components: {
      CustomCursor,
    },
  };
  </script>
  
  <style>
  /* Add your global styles here */
  body {
    cursor: none; /* Hide the default cursor */
  }
  </style>
  