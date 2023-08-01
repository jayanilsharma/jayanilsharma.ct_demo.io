<template>
    <div>
      <h1>Hello, World!</h1>
      <p>This is a placeholder component. You can modify or remove it as needed.</p>
    </div>
    <button @click="onClick">Click Me!</button>
  </template>
  
  <script>
  export default {
    name: 'HelloWorld',
    methods: {
    onClick() {
      alert('Button clicked!');
    },
  }
  };
  </script>
  
  <style>
  /* Add any custom styles for this component */
  </style>
  