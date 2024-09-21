<script setup>
import { ref } from 'vue';

// Reactive reference to control which image to display
const showImage1 = ref(true);

// Form submit handler for showing the "me" image
const showMeImage = (e) => {
  e.preventDefault(); // Prevent default form submission
  showImage1.value = false; 
  showImage1.value = true; 
   // Show the first image ("me.jpeg")
};

// Form submit handler for showing the other image
const showOtherImage = () => {
//   e.preventDefault();

  showImage1.value = true;  // Prevent default form submission
  showImage1.value = false; // Show the second image ("hee.jpeg")
};
setTimeout(() => {
    showImage1.value = true; // After 5 seconds, switch to the second image
  }, 10000); // 5000 milliseconds = 5 seconds

</script>

<template>
  <hr>
  <h1>Me (Arvind) Great ❤🤳</h1>
<h2>This is event Handler and prevent method concept</h2>
  <!-- Form to show the "me" image -->
  <form @submit="showMeImage" >
    <input type="text" placeholder="Please enter your name" />
    <input type="email" placeholder="Please enter your email" />
    <button type="submit">Submit to Show 'Me Image'</button>
  </form>

  <!-- Form to show the other image -->
  <form @submit="showOtherImage" >
    <input type="text" placeholder="Please enter your name" />
    <input type="email" placeholder="Please enter your email" />
    <button type="submit">Submit to Show 'Other Image'</button>
  </form>

  <!-- Conditionally render the images based on the form submission -->
  <div>


        <img class="name"   v-if="showImage1" src="../assets/me.jpeg" alt="First Image" width="300" />
   
    <img class="mame" v-else src="../assets/hee.jpeg" alt="Second Image" width="300"  />
    <h3>This image show reload prevent and stop method </h3>
  </div>
  
</template>

<style >

.name{
    margin-right: 100%;
    border-radius: 50%;
}
.mame{
    margin-left: 80%;
    border-radius: 50%;
}
</style>
