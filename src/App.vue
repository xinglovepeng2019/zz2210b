<template>
  <div>
    <p>姓名:{{ name }}</p>
    <p>年龄{{ age }}</p>
    <button @click="age++">一年又一年</button>
  </div>
</template>

<script setup>
import {reactive,toRefs} from 'vue'
const user =reactive({
  name:"lucy",
  age:12
})
const {name,age} = toRefs(user)
</script>

<style lang="scss" scoped>

</style>