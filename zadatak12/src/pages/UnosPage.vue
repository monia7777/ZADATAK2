<template>
    <div class="q-banner-input">
      <h3>Unesite Q Banner sadržaj</h3>
      <form @submit.prevent="submitForm">
        <div>
          <label for="bannerText">Tekst bannera:</label>
          <input v-model="bannerText" type="text" id="bannerText" placeholder="Unesite tekst za banner" required />
        </div>
        <div>
          <label for="bannerLink">Link za banner:</label>
          <input v-model="bannerLink" type="url" id="bannerLink" placeholder="Unesite link" />
        </div>
        <button type="submit">Pošaljite</button>
      </form>
    </div>
  </template>
  
 