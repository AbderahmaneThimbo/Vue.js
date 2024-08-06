<template>
   <h1>Hello word ! </h1>
   <p>{{ props.user.name }} {{ props.user.age }}</p>
   
 </template>
 
 <script setup>

const props = defineProps(['user']);
 </script>
 
 
 
 <style scoped>
  h1{
    color: blue;
  }
 </style>
 