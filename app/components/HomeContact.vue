<template>
  <div class="kontak_market">
    <div class="container">
       <div class="title_kontak_market">
          <h3>Iki TelurQu semakin mudah didapat</h3>
          <h2>Dapat diborong di toko langgananmu</h2>
       </div>

       <div class="list_market">
          <h4>Toko Online <span>(klik logo untuk membeli)</span></h4>
          <div class="row">
             <div class="col-xs-6 col-sm-6 col-md-3 col-lg-3 mb-20" v-for="(shop, i) in onlineShops" :key="i">
                <a :href="shop.url" target="_blank">
                   <div class="box_kontak_market">
                      <img :src="shop.img" class="img-responsive" alt="Image">
                   </div>
                </a>
             </div>
          </div>
       </div>

       <div class="list_swalayan">
           <!-- Swalayan list truncated for brevity, focusing on structure -->
           <h4>Supermarket, Swalayan & Toko Oleh-oleh :</h4>
           <!-- Grid similar to above -->
       </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const onlineShops = [
    { url: '#', img: 'https://ikitelurqu.com/asset_front/img/produk/store_shopee.png' },
    { url: '#', img: 'https://ikitelurqu.com/asset_front/img/produk/store_tokped.png' },
    { url: '#', img: 'https://ikitelurqu.com/asset_front/img/produk/store_tiktok.png' },
    { url: '#', img: 'https://ikitelurqu.com/asset_front/img/produk/store_whatsapp.png' }
]
</script>

<style scoped>
.kontak_market {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: var(--color-bg-light);
}

.title_kontak_market {
  padding-bottom: 60px;
  text-align: center;
}

.title_kontak_market h3 { margin: 0; color: var(--color-grey); }
.title_kontak_market h2 { margin: 0; color: var(--color-blue); font-family: var(--font-baloo); font-weight: 700; }

.list_market h4 { text-align: center; margin-bottom: 30px; }
.list_market h4 span { color: var(--color-red); }

.box_kontak_market {
  width: 100%;
  background: white;
  box-shadow: -1px 8px 12px -4px rgba(105,105,105,0.2);
  padding: 10px;
  height: 100px;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: background 0.2s;
}

.box_kontak_market:hover {
    background-color: var(--color-bg-light);
}

.box_kontak_market img {
    max-height: 100%;
    max-width: 100%;
}

.mb-20 { margin-bottom: 20px; }
</style>
