<script setup>

import { reactive, ref } from 'vue';
// const b=ref("")
const b = reactive({
    value: " "
})


const aman = reactive({ val: { count: 0 }, arr: ['aman', 'shyam'] })

const addUser = () => {
    aman.arr[2] = 'aman❤'
    aman.arr[3] = 'Aditi'
    aman.arr[4] = 'Ramana'
}
const Delete = () => {
    aman.arr[2] = ''
    aman.arr[3] = ''
    aman.arr[4] = ''
}

const add = () => {
    aman.arr.push(b.value)
}
console.log(b.value)



</script>



<template>
    <hr>
    <h2>This is reactivity concept</h2>
    <h1>count: {{ aman.val.count }}</h1>
    <h2>User:{{ aman.arr }}</h2>

    <button @click="aman.val.count++">Add +</button>
    <button @click="addUser">Add one more user +</button>
    <button @click="Delete">Delete User name </button>
    <button @click="aman.val.count--">Sub -</button>
    <form @submit.prevent="add">
        <input type="text" placeholder="add users from here" v-model="b.value">
        <input type="submit" value="Add User name from yourside">
    </form>

    <hr>
</template>
