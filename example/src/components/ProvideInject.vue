<script setup>
import { inject } from 'vue';
const aman = inject('game')


</script>

<template>
<hr>
<h1> provide Inject</h1>

<ul v-for="(aman, i) in aman" :key="i">
    <li>{{aman}}</li>
</ul>
</template>