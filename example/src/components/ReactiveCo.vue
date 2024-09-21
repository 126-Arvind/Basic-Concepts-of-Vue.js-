<script setup>

import { reactive } from 'vue';

const count= reactive({ coun : 0 })


</script>


<template>
<h1>count: {{ count.coun }}</h1>
<button @click="count.coun ++">+</button>
<button @click="count.coun --">-</button>


<h3>Example Event Handlers and Reactivity , reference</h3>

</template>



