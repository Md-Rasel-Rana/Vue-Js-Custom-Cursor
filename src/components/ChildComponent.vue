<template>
    <div>
      <h3>Child Component</h3>
      <!-- Display the value of the 'message' prop -->
      <p>{{ message }}</p>
      <p>parent name is {{ parentname }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ['message','parentname'], // Declare a prop named 'message'
  };
  </script>
  