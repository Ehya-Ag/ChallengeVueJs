<template>

<!-- <div
v-if="user.age>35"
> mon age
</div>
<div
v-else="user.age>15"
> else
</div> -->
<helloworld />

<div class="text-green">
  {{user.name}}
</div>
</template>
  <template v-slot:name>
    {{user.name}}
  </template>
  <template v-slot:age>
    {{user.age}}
  </template>

<!-- {{ subTitle }}
<input type="text" v-model="user.name" @input="display">
<input type="text" v-model="user.age"> -->
</template>
<script setup>
import helloworld from '@/components/helloworld.vue';
import { reactive } from 'vue';

const user = reactive ( {
name: "Ehya ag mohamed",
age: 24, });

const display = () =>{
console.log(user.name, user.age);
}
</script>



<style scoped>

  .text-red {
    color:brown;
  }
    .text-green {
    color:rgb(23, 197, 116);
  }
</style>


//Les slots 
//APP 
<template>
  <helloworld>
    <p>
      {{user.name}}
    </p>

  <div class="text-green">
    {{user.name}}
  </div>
   <template v-slot:name>
    {{user.name}}
  </template>
  <template v-slot:age>
    {{user.age}}
  </template> 
  </helloworld>
</template>
<script setup >
  import helloworld from '@/components/helloworld.vue';
  import { reactive } from 'vue';

  const user = reactive( {
    name: 'Ehya Ag Mohamed',
    age: 30
});
const display = () =>{
  console.log(user.name, user.age)
}
display();
</script>
<style scoped>
.text-red{
  color: red;
}
.text-green{
  color: green;
}
</style>

//helloworld


<template>
<h1>Bonjour</h1>
<slot name="name">

</slot>
<slot name="age">

</slot>
</template>

<script setup >

</script>

<style scoped>
h1{
    color: aqua;
}
</style>
