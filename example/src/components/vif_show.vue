<script setup>
    import { ref } from 'vue'
    const num = ref(7)
</script>

<template>
<hr>
<h3>This is v-if , v-show, v-else-if, v-else, v-for section</h3>
  <h5>v-if : if this statemetn false then on screen or on inspect under element no state is there to show v-if <br> v-show : if this state is false then under inspect -element we will see false false statement like as alt in css.</h5>  
<div>
        <input type="number" v-model="num"/>
        <p v-if="num>5">IF</p>
        <p v-show="num>5">hello g kaisa hai </p>
        <!-- <p v-else>Bye</p> -->


    </div>
<hr>
</template>