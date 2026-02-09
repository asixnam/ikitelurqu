<template>
  <div class="maps-container">
    <div class="container">
      <div class="row">
        <div class="col-md-12 text-center">
          <span class="sub-title">Mudah Didapat</span>
          <h2>Dapatkan di Toko Langgananmu</h2>
          <p class="section-desc">Tersedia secara online maupun offline di berbagai supermarket dan toko oleh-oleh.</p>
          
          <h3 class="share-title">Bagikan informasi outlet Iki TelurQu ke temanmu</h3>
          
          <div class="share-buttons">
            <a :href="whatsappLink" target="_blank" class="share-btn whatsapp" title="Bagikan ke WhatsApp">
              <i class="fa fa-whatsapp"></i>
            </a>
            <a :href="telegramLink" target="_blank" class="share-btn telegram" title="Bagikan ke Telegram">
              <i class="fa fa-telegram"></i>
            </a>
            <button @click="copyLink" class="share-btn copy-link" title="Salin Tautan">
              <i class="fa fa-link"></i>
            </button>
          </div>

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

const whatsappLink = computed(() => {
  return `https://api.whatsapp.com/send?text=${encodeURIComponent(shareText + mapUrl)}`
})

const telegramLink = computed(() => {
  return `https://t.me/share/url?url=${encodeURIComponent(mapUrl)}&text=${encodeURIComponent(shareText)}`
})

const copyLink = async () => {
  try {
    await navigator.clipboard.writeText(mapUrl)
    alert('Tautan berhasil disalin!')
  } catch (err) {
    console.error('Failed to copy: ', err)
  }
}
</script>

<style scoped>
.maps-container {
  padding: 80px 0; /* Increased padding */
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
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 24px;
  transition: all 0.3s ease;
  border: none;
  cursor: pointer;
  text-decoration: none;
}

.share-btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.2);
  color: #fff;
}

.whatsapp {
  background-color: #25D366;
}

.telegram {
  background-color: #0088cc;
}

.copy-link {
  background-color: #888;
}

.map-wrapper {
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 5px 10px rgba(0,0,0,0.1);
  background: #eee;
  height: 500px;
}

.map-wrapper iframe {
  display: block; /* Removes bottom space of iframe */
  height: 100%;
}

/* Mobile Responsiveness */
@media (max-width: 767px) {
  .maps-container {
    padding: 100px 0;
  }
  
  h2 {
    font-size: 28px;
  }
  
  .section-desc {
    font-size: 14px;
    margin-bottom: 30px;
  }
  
  .share-buttons {
    gap: 10px;
  }
  
  .share-btn {
    width: 40px;
    height: 40px;
    font-size: 20px;
  }
  
  .map-wrapper {
    height: 350px;
  }
}

</style>
