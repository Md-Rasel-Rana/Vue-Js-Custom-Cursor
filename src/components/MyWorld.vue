<template>
    <div>
      <div>
        <h1 :class="{green: colorchange}">hello</h1>
        <button @click="changeColor">click me</button>
      </div>
      <img :src="url" :alt="alt">
    </div>
  </template>
  
  <script>
  export default {
    name: 'MyWorld',
    data() {
      return {
        url: 'https://picsum.photos/id/237/200/300/',
        alt: 'image',
        colorchange: false // Make sure to add a comma after 'alt' property
      };
    },
    methods:{
      changeColor() {
        this.colorchange = !this.colorchange; 
      }
    }
  };
  </script>
  
  <style>
  /* Add any necessary styles here */
  .green {
    background-color: green;
    color: white;
    padding: 10px;
    border-radius: 5px;
    width: 200px;
  }
  .red {
    background-color: red;
    color: white;
    padding: 10px;
    border-radius: 5px;
    width: 400px;
  }
  </style>
  