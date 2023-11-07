<script setup>
  import { ref } from 'vue';
  
  const selectedOption = ref('');
  </script>

<template>
    <div class="gender-selector">
      <h1 class="title">Gender Selector</h1>
      <div class="select-container">
        <label for="gender-select">Select Gender:</label>
        <select id="gender-select" v-model="selectedOption">
          <option value="1">Male</option>
          <option value="2">Female</option>
          <option value="3">Other</option>
        </select>
      </div>
      <div class="gender-info">
        <p v-if="selectedOption === '1'">You selected: Male</p>
        <p v-else-if="selectedOption === '2'">You selected: Female</p>
        <p v-else>You selected: Other</p>
      </div>
  
      <hr>
  
      <h2 class="additional-info-title">Additional Information</h2>
      <div class="additional-info">
        <p v-if="selectedOption === '1'">Hi, I'm Trex.</p>
        <p v-else-if="selectedOption === '2'">Hi, I'm Trexie.</p>
        <p v-else>Hi, I'm alien.</p>
      </div>
    </div>
  </template>
  
  
  
  <style>
#app {
    width: 100%;
    height: 100vh;
    background-image: url(/venjo.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
}

  .gender-selector {
    font-family: Arial, sans-serif;
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    backdrop-filter: blur(5px) saturate(150%);
    -webkit-backdrop-filter: blur(5px) saturate(150%);
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 12px;
    border: 1px solid rgba(209, 213, 219, 0.3);
  }
  
  .title {
    font-size: 24px;
    margin-bottom: 10px;
  }
  
  .select-container {
    margin-bottom: 20px;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
  }
  
  #gender-select {
    width: 100%;
    padding: 8px;
    border: 1px solid #f80606;
    border-radius: 4px;
  }
  
  .gender-info {
    font-size: 18px;
    margin-bottom: 20px;
  }
  
  .additional-info-title {
    font-size: 20px;
    margin-bottom: 10px;
  }
  
  .additional-info {
    font-size: 16px;
  }
  
  </style>
  
  

  