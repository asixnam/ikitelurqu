<template>
  <div class="testimoni section-padding bg-gray">
     <div class="container">
        <div class="section-title text-center mb-50">
           <span class="sub-title">Kata Mereka</span>
           <h2>Testimoni Pelanggan</h2>
           <div class="star-rating mt-20">
              <i class="glyphicon glyphicon-star"></i>
              <i class="glyphicon glyphicon-star"></i>
              <i class="glyphicon glyphicon-star"></i>
              <i class="glyphicon glyphicon-star"></i>
              <i class="glyphicon glyphicon-star"></i>
           </div>
        </div>

        <div class="row">
           <div class="col-md-3 col-sm-6 mb-30" v-for="(img, i) in testimoniImgs" :key="i">
              <div class="testimoni-card">
                 <div class="card-img">
                    <img :src="img" alt="Testimoni Customer" class="img-responsive">
                 </div>
              </div>
           </div>
        </div>
     </div>
  </div>
</template>

<script setup lang="ts">
const testimoniImgs = [
  'https://ikitelurqu.com/asset_front/img/testimoni/testimoni_ikitelurqu_1.png',
  'https://ikitelurqu.com/asset_front/img/testimoni/testimoni_ikitelurqu_2.png',
  'https://ikitelurqu.com/asset_front/img/testimoni/testimoni_ikitelurqu_3.png',
  'https://ikitelurqu.com/asset_front/img/testimoni/testimoni_ikitelurqu_4.png'
]
</script>

<style scoped>
.bg-gray {
  background-color: var(--bg-gray);
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

.star-rating {
  color: #ffc107;
  font-size: 20px;
}

.star-rating i {
  margin: 0 2px;
}

.testimoni-card {
  background: #fff;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 5px 20px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  height: 100%;
}

.testimoni-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 30px rgba(0,0,0,0.1);
}

.card-img img {
  width: 100%;
  height: auto;
  display: block;
}

.mb-30 { margin-bottom: 30px; }
.mt-20 { margin-top: 20px; }
</style>
