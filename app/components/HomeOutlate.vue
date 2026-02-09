<template>
  <div class="kontak_market section-padding bg-light">
    <div class="container">
       <div class="list_market mb-50">
          <h4 class="text-center mb-30">Toko Online</h4>
          <div class="row market-grid">
             <div class="col-xs-6 col-sm-3 mb-20" v-for="(shop, i) in onlineShops" :key="i">
                <a :href="shop.url" target="_blank" class="market-box">
                   <img :src="shop.img" class="img-responsive" :alt="shop.name">
                </a>
             </div>
          </div>
       </div>

       <div class="list_swalayan">
           <h4 class="text-center mb-30">Supermarket & Toko Oleh-oleh</h4>
           <div class="row market-grid">
               <div class="col-xs-4 col-sm-3 mb-20" v-for="(item, i) in swalayan" :key="i">
                  <div class="market-box small">
                     <img :src="item.img" class="img-responsive" alt="Outlet Partner">
                  </div>
               </div>
           </div>
           
           <div class="text-center mt-40">
              <NuxtLink to="/outlet" class="btn-theme">Lihat Lokasi Outlet</NuxtLink>
           </div>
       </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const onlineShops = [
    { name: 'Shopee', url: 'https://shopee.co.id/ikienak', img: 'https://ikitelurqu.com/asset_front/img/produk/store_shopee.png' },
    { name: 'Tokopedia', url: 'https://www.tokopedia.com/keripikpuyuh', img: 'https://ikitelurqu.com/asset_front/img/produk/store_tokped.png' },
    { name: 'TikTok Shop', url: 'https://www.tiktok.com/@ikitelurqu', img: 'https://ikitelurqu.com/asset_front/img/produk/store_tiktok.png' },
    { name: 'WhatsApp', url: 'https://api.whatsapp.com/send?phone=6282190000716', img: 'https://ikitelurqu.com/asset_front/img/produk/store_whatsapp.png' }
]

const swalayan = [
    { img: 'https://ikitelurqu.com/asset_front/img/market/progo.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/mana_kampus.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/pamela.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/gardena.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/purnama.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/januputra.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/mulia_toserba_bantul.png' },
    { img: 'https://ikitelurqu.com/asset_front/img/market/plaza_argo.png' }
]
</script>

<style scoped>
.bg-light {
  background-color: #f9f9f9;
}

.sub-title {
  color: var(--theme-color);
  font-family: var(--font-poppins);
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.section-title h2 {
  font-family: var(--font-poppins);
  font-weight: 700;
  font-size: 36px;
  color: var(--heading-color);
  margin-top: 5px;
}

h4 {
  font-family: var(--font-poppins);
  font-weight: 600;
  color: var(--heading-color);
}

.market-box {
  background: #fff;
  border-radius: 8px;
  padding: 15px;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100px; /* Fixed height for consistency */
  box-shadow: 0 2px 10px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
}

.market-box:hover {
  transform: translateY(-3px);
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.market-box img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.market-box.small {
  height: 80px;
  padding: 10px;
}

.btn-theme {
  display: inline-block;
  margin-top: 20px;
}

.mt-40 { margin-top: 40px; }
.mb-20 { margin-bottom: 20px; }
.mb-30 { margin-bottom: 30px; }
.mb-50 { margin-bottom: 50px; }
</style>
