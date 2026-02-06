<template>
  <div class="produk">
    <div class="container">
       <div class="title_produk">
          <h3>Pilih sesuai dengan kebutuhanmu</h3>
          <h2>Pilihan produk Iki TelurQu</h2>
       </div>

       <div class="list_produk">
          <div class="row">
             <div class="col-xs-12 col-sm-12 col-md-4 col-lg-4 mb-30" v-for="(product, i) in products" :key="i">
                <div class="box_label_produk">
                   <div :class="['label_produk', product.bgClass]">
                      <h3>{{ product.name }}</h3>
                   </div>
                   <div class="img_produk">
                      <img :src="product.img" class="img-responsive" alt="Image">
                   </div>
                   <div class="deskripsi_produk">
                      <hr>
                      <div class="row info-grid">
                         <div class="col-xs-6 mb-10" v-for="(detail, k) in product.details" :key="k">
                            <div class="icon_pack">
                               <p>{{ detail }}</p>
                            </div>
                         </div>
                      </div>
                   </div>
                </div>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const products = [
  {
    name: 'Kemasan Ecer',
    bgClass: 'bg_label_produk_yellow',
    img: 'https://ikitelurqu.com/asset_front/img/produk/iki_telurqu_ecer.png',
    details: ['Kemasan ecer', '4 & 5 butir', '1 pack', 'Rasa Bacem']
  },
  {
    name: 'Kemasan Display',
    bgClass: 'bg_label_produk_orange',
    img: 'https://ikitelurqu.com/asset_front/img/produk/iki_telurqu_display%203_1.png',
    details: ['Kemasan ecer', '4 & 5 butir', '15 pack', 'Rasa Bacem']
  },
  {
    name: 'Kemasan Premium',
    bgClass: 'bg_label_produk_red',
    img: 'https://ikitelurqu.com/asset_front/img/produk/iki_telurqu%20premium2_1.png',
    details: ['Kemasan ecer', '5 butir', '5 pack', 'Rasa Bacem']
  }
]
</script>

<style scoped>
.produk {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: var(--color-bg-light);
}

.title_produk {
  padding-bottom: 80px;
  text-align: center;
}

.title_produk h3 { margin: 0; color: var(--color-grey); }
.title_produk h2 { margin: 0; color: var(--color-blue); font-family: var(--font-baloo); font-weight: 700; }

.box_label_produk {
  background: white;
  border-radius: 10px;
  box-shadow: -1px 8px 12px -4px rgba(105,105,105,0.2);
  padding-bottom: 20px;
  overflow: hidden;
}

.label_produk { padding: 20px; }
.label_produk h3 { color: white; margin: 0; text-align: center; font-family: var(--font-baloo); font-weight: 700; }

.bg_label_produk_yellow { background-color: var(--color-yellow); }
.bg_label_produk_orange { background-color: var(--color-orange); }
.bg_label_produk_red { background-color: var(--color-red); }

.img_produk {
  height: 300px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.img_produk img {
  max-height: 100%;
  max-width: 80%;
}

.deskripsi_produk { padding: 0 30px; }
.deskripsi_produk hr { border-top: 2px solid var(--color-grey); margin: 20px 0; }

.icon_pack p {
  font-family: var(--font-baloo);
  margin: 0;
  text-align: center;
  font-size: 14px;
}

.mb-30 { margin-bottom: 30px; }
.mb-10 { margin-bottom: 15px; }
.info-grid {
    display: flex;
    flex-wrap: wrap;
}
.col-xs-6 {
    width: 50%;
}
</style>
