<template>
  <div class="maps-container">
    <div class="container">
      <div class="row">
        <div class="col-md-12 text-center">
          
          <h2>Mudah Dapatkan Iki TelurQu</h2>
          <p class="section-desc">Tersedia secara online maupun offline di berbagai supermarket dan toko oleh-oleh.</p>
          
          <h3 class="share-title">Kamu bisa dapatkan Iki TelurQu dengan klik aja</h3>
          
          <div class="share-buttons">
            <a :href="whatsappLink" target="_blank" class="share-btn whatsapp-btn">
              <i class="fa fa-whatsapp"></i> <span>WhatsApp</span>
            </a>
            <a :href="shopeeLink" target="_blank" class="share-btn shopee-btn">
              <i class="fa fa-shopping-bag"></i> <span>Shopee</span>
            </a>
          </div>
          <h3 class="share-title">Tersedia di beberapa toko di DI Yogykarta dan sekitarnya</h3>

          <div class="map-wrapper">
             <iframe 
               src="https://www.google.com/maps/d/embed?mid=1HM8rtZHEhK-dG8Xxb679wWXJTeboWVA&ehbc=2E312F" 
               width="100%" 
               height="500"
               style="border:0;"
               allowfullscreen=""
               loading="lazy">
             </iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { computed } from 'vue'

const mapUrl = 'https://www.google.com/maps/d/u/0/viewer?mid=1HM8rtZHEhK-dG8Xxb679wWXJTeboWVA'
const shareText = 'Cek lokasi outlet Iki TelurQu di sini: '
const shopeeLink = 'https://shopee.co.id/ikienak'

const whatsappLink = computed(() => {
  return `https://api.whatsapp.com/send?text=${encodeURIComponent(shareText + mapUrl)}`
})
</script>

<style scoped>
.maps-container {
  padding: 80px 0;
  background: #fff;
}

.sub-title {
  color: var(--theme-color);
  font-family: var(--font-poppins);
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
  display: block;
  margin-bottom: 5px;
}

h2 {
  font-family: var(--font-poppins);
  font-weight: 700;
  font-size: 36px;
  color: var(--heading-color);
  margin-bottom: 15px;
  line-height: 1.2;
}

.section-desc {
  color: #666;
  font-size: 16px;
  max-width: 600px;
  margin: 0 auto 40px;
  line-height: 1.6;
}

.share-title {
  font-family: var(--font-poppins);
  font-weight: 600;
  color: #333;
  margin-bottom: 20px;
  font-size: 18px;
}

.share-buttons {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-bottom: 40px;
}

.share-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  padding: 12px 30px;
  border-radius: 8px; /* Slightly rounded */
  color: #fff;
  font-family: var(--font-poppins);
  font-weight: 600;
  font-size: 16px;
  text-decoration: none;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  min-width: 160px;
}

.share-btn i {
  font-size: 20px;
}

.share-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
  color: #fff;
}

.whatsapp-btn {
  background-color: #25D366; /* WhatsApp Green */
}

.shopee-btn {
  background-color: #EE4D2D; /* Shopee Orange */
}

.map-wrapper {
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 5px 10px rgba(0,0,0,0.1);
  background: #eee;
  height: 500px;
}

.map-wrapper iframe {
  display: block;
  height: 100%;
}

/* Mobile Responsiveness */
@media (max-width: 767px) {
  .maps-container {
    padding: 60px 0;
  }
  
  h2 {
    font-size: 28px;
  }
  
  .section-desc {
    font-size: 14px;
    margin-bottom: 30px;
  }
  
  .share-buttons {
    flex-direction: column;
    align-items: center;
    gap: 15px;
  }
  
  .share-btn {
    width: 100%;
    max-width: 250px;
  }
  
  .map-wrapper {
    height: 350px;
  }
}
</style>
