<template>
  <div class="produk section-padding">
    <div class="container">
       <div class="section-title text-center mb-50">
          <span class="sub-title">Pilih sesuai kebutuhanmu</span>
          <h2>Pilihan Produk Iki TelurQu</h2>
       </div>

       <div class="row">
          <div class="col-md-4 col-sm-6 mb-30" v-for="(product, i) in products" :key="i">
             <div class="product-card">
                <div class="product-header" :class="product.colorClass">
                   <h3>{{ product.name }}</h3>
                </div>
                
                <div class="product-img">
                   <img :src="product.img" class="img-responsive" :alt="product.name">
                </div>
                
                <div class="product-body">
                   <div class="specs-grid">
                      <div class="spec-item" v-for="(detail, k) in product.details" :key="k">
                         <span class="icon"><i class="glyphicon glyphicon-ok-sign"></i></span>
                         <span class="text">{{ detail }}</span>
                      </div>
                   </div>
                   
                   <div class="action-btn text-center mt-30">
                      <NuxtLink to="/products" class="btn-border">Lihat Detail</NuxtLink>
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
    colorClass: 'theme-orange',
    img: 'https://ikitelurqu.com/asset_front/img/produk/iki_telurqu_ecer.png',
    details: ['Isi 4 & 5 butir', 'Kemasan Ecer', 'Min. 1 pack', 'Rasa Bacem Khas']
  },
  {
    name: 'Kemasan Display',
    colorClass: 'theme-orange',
    img: 'https://ikitelurqu.com/asset_front/img/produk/iki_telurqu_display%203_1.png',
    details: ['Isi 4 & 5 butir', 'Kemasan Display', 'Isi 15 pack', 'Rasa Bacem Khas']
  },
  {
    name: 'Kemasan Premium',
    colorClass: 'theme-orange',
    img: 'https://ikitelurqu.com/asset_front/img/produk/iki_telurqu%20premium2_1.png',
    details: ['Isi 5 butir', 'Kemasan Premium', 'Isi 5 pack', 'Rasa Bacem Khas']
  }
]
</script>

<style scoped>
.produk {
  background-color: var(--white);
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

.product-card {
  background: #fff;
  border: 1px solid #eee;
  border-radius: 8px;
  overflow: hidden;
  transition: all 0.3s ease;
  height: 100%;
}

.product-card:hover {
  box-shadow: 0 10px 25px rgba(0,0,0,0.08);
  border-color: transparent;
  transform: translateY(-5px);
}

.product-header {
  padding: 15px;
  text-align: center;
  background: var(--bg-gray);
}

.product-header h3 {
  margin: 0;
  font-size: 20px;
  font-weight: 600;
  color: var(--heading-color);
}

.product-header.theme-orange h3 {
  color: var(--theme-color);
}

.product-img {
  height: 250px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  background: #fff;
}

.product-img img {
  max-height: 100%;
  max-width: 100%;
  transition: transform 0.3s;
}

.product-card:hover .product-img img {
  transform: scale(1.05);
}

.product-body {
  padding: 0 25px 30px;
}

.specs-grid {
  display: flex;
  flex-wrap: wrap;
  border-top: 1px solid #f0f0f0;
  padding-top: 20px;
}

.spec-item {
  width: 50%;
  margin-bottom: 15px;
  display: flex;
  align-items: center;
  font-size: 14px;
  color: #666;
}

.spec-item .icon {
  color: var(--theme-color);
  margin-right: 8px;
}

.mt-30 { margin-top: 30px; }
</style>
