<template>
  <div>
我是子组件 {{ money }}--{{ car }}
<button @click="change">更改价格</button>
  </div>
</template>

<script setup>
const props = defineProps({
  money:Number,
  car:String
})

// js中使用props
// console.log(props.money)

// 1.得到emit函数，显性声明事件名称
const emit =defineEmits(['changeMoney'])

const change = ()=>{
  // 通知父组件进行更改
  emit('changeMoney',10)
}
</script>

<style lang="scss" scoped>

</style>