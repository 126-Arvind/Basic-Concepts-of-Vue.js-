<script setup>
import { ref } from 'vue'
const aman_aditi = ref("")
const username = ref()
const name=ref()

const done = () => {
  name.value= username.value
  
}
</script>


<template>

    <div>
        <hr>
        <h2>This is a Ref component example </h2>
       
        <h3> Username: {{ name}} {{ aman_aditi }}</h3>

        <form @submit.prevent="done">
            <h3>{{ username }}</h3>
            <input type="text" placeholder="Enter your user name here" v-model="username">
            <button type="submit">submit</button>
        </form>


        <button @click="aman_aditi = 'Aman❤Aditi'">Click the button and see what?🤔</button>
    </div>
</template>


