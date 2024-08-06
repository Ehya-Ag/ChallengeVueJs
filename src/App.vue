<template>
  <helloworld 
  @update-name ="name => display(name)"
  />
</template>
<script setup >
  import helloworld from '@/components/helloworld.vue';
  import { watch, computed, ref } from 'vue';
  const display = (name) =>{
  console.log('App.vue : ' + name)
}


</script>
<style scoped>
.text-red{
  color: red;
}
.text-green{
  color: green;
}
.bold{
  font-size: 1rem;
}
</style>