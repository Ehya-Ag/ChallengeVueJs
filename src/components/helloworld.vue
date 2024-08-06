<template>
<h1>Bonjour</h1>
{{name}}

<input type="text" v-model="name" @import="handleUpdate">
</template>

<script setup >
import { ref } from "vue"

const emit = defineEmits(['updateName'])
const handleUpdate= (event) =>{
    console.log(event.target.value)
}
const name = ref('')
</script>

<style scoped>
h1{
    color: aqua;
}
</style>
