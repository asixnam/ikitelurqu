<template>
  <div class="feed_sosial_media">
     <div class="container">
        <div class="title_feed">
           <h3>Info produk dan promo follow kami</h3>
           <h2>Instagram @ikitelurqu</h2>
        </div>

        <div class="box_feed">
           <div class="elfsight-app-1e154510-db87-4079-a5a5-b0f6b1c34eea" data-elfsight-app-lazy></div>
        </div>
     </div>
  </div>
</template>

<script setup lang="ts">
import { useHead } from '#imports'

useHead({
  script: [
    {
      src: 'https://static.elfsight.com/platform/platform.js',
      'data-use-service-core': true,
      defer: true
    }
  ]
})
</script>

<style scoped>
.feed_sosial_media {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: var(--color-bg-light);
}

.title_feed {
  padding-bottom: 60px;
  text-align: center;
}

.title_feed h3 { margin: 0; color: var(--color-grey); }
.title_feed h2 { 
  margin: 0; 
  color: var(--color-blue); 
  font-family: var(--font-baloo); 
  font-weight: 700; 
  font-size: 40px;
}
</style>
