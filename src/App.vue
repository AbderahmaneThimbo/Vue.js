<template> 
       <Hello :user="user"/>
     
       <!-- <div v-if="user.age > 15">
         Mon age
       </div>
       <div v-else>
         Else
       </div> -->
       <div :class="[user.age > 30 ? 'text-red' : 'text-green']">
         {{ user.name }}
       </div>
       
     <input type="text" v-model="user.name" v-on:input="display">
     <input type="text" v-model="user.age">

</template>

<script setup>
import Hello from './components/Hello.vue';

import { reactive } from 'vue';

const user = reactive({
   name: 'Coders',
   age:65,
});

const display = () => {
   console.log(user.name,user.age);
   
}

</script>



<style scoped>

.text-red {
   color:red;
}
.text-green{
   color: green;
}
</style>
