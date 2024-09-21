<script setup >
import {ref } from 'vue'
const user = ref('')
const email = ref('')
const password = ref('')


</script>
<template>

<button @click="$emit('incrementCounter')">+</button>
<form @submit.prevent="$emit('userinfo', user, email, password )">
<input type="text" v-model="user">
<input type="email" v-model="email">
<input type="password" v-model="password">
<button type="submit"> submit</button>



</form>


</template>