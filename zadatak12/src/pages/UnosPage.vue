<template>
    <div class="banner-container">
      <div v-if="isVisible" class="banner">
        <div class="banner-content">
          <input
            v-model="bannerText"
            :placeholder="placeholder"
            class="banner-input"
            @input="handleInputChange"
          />
          <button @click="submitBanner" class="banner-button">Submit</button>
        </div>
      </div>
      <button v-if="!isVisible" @click="showBanner" class="show-banner-btn">Show Banner</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        bannerText: "",
        isVisible: false,
        placeholder: "Enter your banner text here..."
      };
    },
    methods: {
      handleInputChange() {
        // Optional: You can add logic here to handle input change
      },
      submitBanner() {
        alert(`Banner Submitted: ${this.bannerText}`);
        this.isVisible = false; // Hide banner after submission
      },
      showBanner() {
        this.isVisible = true;
      }
    }
  };
  </script>
  
  <style scoped>
  .banner-container {
    text-align: center;
    margin-top: 20px;
  }
  
  .banner {
    background-color: #ffcc00;
    padding: 10px;
    border-radius: 5px;
    display: inline-block;
  }
  
  .banner-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  
  .banner-input {
    padding: 8px;
    font-size: 16px;
    margin-right: 10px;
  }
  
  .banner-button {
    padding: 8px 16px;
    font-size: 16px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .show-banner-btn {
    padding: 10px 20px;
    background-color: #008CBA;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  </style>
  