<template>
    <div>
        <h1>v-for LOOP</h1>
      <h2>Product Rating:</h2>
      <span v-for="star in rating" :key="star">⭐😊</span>
    </div>
  </template>
  
  <script setup>
  const rating = 4; // The product has a 4-star rating
  </script>