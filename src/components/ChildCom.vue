<template>
    <div class="app-page" 
    style="border:10px solid #ccc;
    padding:50px;
    width:100px">
      child组件{{ count }}
      <button @click="updateCount(100)">修改count</button>
    </div>
   </template>
   
   <script setup>
   import {inject} from 'vue'
   let count =inject('count')
   const updateCount = inject('updateCount')


   </script>
   
   <style lang="scss" scoped>
   
   </style>