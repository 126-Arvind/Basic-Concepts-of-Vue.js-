<script setup>

import { onBeforeMount, onMounted, onBeforeUnmount, onBeforeUpdate, onUnmounted, onUpdated , ref} from 'vue';

const message = ref( 'hello worold')


onMounted(()=>{
    
    console.log('onMounted')
})
// here onbeforemount function call first then other function executed
// that's why in console first onbeforemount run then onmounted run
onBeforeMount( () =>{
    console.log('onBefore Mount')
})

onBeforeUpdate(()=>{
console.log('onBeforeUpdated')
})

const update= ()=>{
    message.value= 'updated Message'
}

onUpdated (() =>{
    console.log( 'it wait component to be update after that is call')
})
</script>
<template>

<h1>LifeCycle of Components</h1>
<p>{{message}}</p>
<button @click="update">Update now</button>
</template>