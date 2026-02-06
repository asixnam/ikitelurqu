<template>
  <div class="testimoni">
     <div class="container">
        <div class="title_testimoni">
           <h3>Penilaian customer kami</h3>
           <h2>Testimoni Iki TelurQu</h2>
           <div class="star">
              <span class="glyphicon glyphicon-star" aria-hidden="true"></span>
              <span class="glyphicon glyphicon-star" aria-hidden="true"></span>
              <span class="glyphicon glyphicon-star" aria-hidden="true"></span>
              <span class="glyphicon glyphicon-star" aria-hidden="true"></span>
              <span class="glyphicon glyphicon-star" aria-hidden="true"></span>
           </div>
        </div>

        <div class="side-testimoni row">
            <!-- Simplified grid without carousel JS for now, or nice flex scroll -->
           <div class="col-md-3 col-sm-6 mb-20" v-for="(img, i) in testimoniImgs" :key="i">
              <div class="card-content">
                 <div class="img_testimoni">
                    <img :src="img" alt="" class="img-responsive">
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
.testimoni {
  padding-top: 100px;
  padding-bottom: 100px;
}

.title_testimoni {
  padding-bottom: 60px;
  text-align: center;
}

.title_testimoni h3 { margin: 0; color: var(--color-grey); }
.title_testimoni h2 { 
  margin: 0; 
  color: var(--color-blue); 
  font-family: var(--font-baloo); 
  font-weight: 700; 
  font-size: 40px;
}

.star .glyphicon-star {
  color: var(--color-gold);
  font-size: 20px;
  margin: 0 2px;
}

.card-content {
  padding: 10px;
  background: #fff;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.mb-20 { margin-bottom: 20px; }
</style>
