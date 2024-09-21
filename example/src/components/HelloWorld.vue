<script setup >
import { ref } from 'vue';

const v= ref({a:[1]})
console.log(v.a)
</script>

<template>
    <h1>Hello friends</h1>
<h1>{{v.a}}</h1>
<h1>{{v.a=10}}</h1>
<h5> Here is the log how we can change value of a=1 to a=10 in console a=1 but at time of calling v.a=10</h5>

</template>