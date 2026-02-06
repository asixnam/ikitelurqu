<template>
  <div class="produksi">
    <div class="container">
       <div class="title_produksi">
          <h3>Pengolahan modern</h3>
          <h2>Diolah secara modern & Otomatis</h2>
       </div>
       
       <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-3 col-lg-3 mb-30">
             <div class="box_img_produksi">
                <div class="video_produksi">
                    <!-- Placeholder video/image -->
                    <div style="background:#000; height: 300px; width:100%; display:flex; align-items:center; justify-content:center; color:white;">VIDEO</div>
                </div>
             </div>
          </div>

          <div class="col-xs-12 col-sm-12 col-md-3 col-lg-3 mb-30" v-for="(item, i) in steps" :key="i">
             <div class="box_img_produksi">
                <div class="img_produksi">
                   <img :src="item.img" class="img-responsive" alt="Image">
                </div>
                <div class="text_deskripsi_produksi">
                   <h3>{{ item.title }}</h3>
                   <span><hr></span>
                   <p>{{ item.desc }}</p>
                </div>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const steps = [
  {
    title: 'Proses Rebus memakai mesin Otomatis',
    desc: 'Tahapan proses perebusan dengan suhu dan waktu yang tepat...',
    img: 'https://ikitelurqu.com/asset_front/img/produksi_perebusan_otomatis.png'
  },
  {
    title: 'Proses Kupas memakai mesin Otomatis',
    desc: 'Untuk mengurangi kerusakan pada telur, proses kupas telur puyuh telah memakai mesin otomatis...',
    img: 'https://ikitelurqu.com/asset_front/img/produksi_kupas_otomatis.png'
  },
  {
    title: 'Sterilisasi Retort suhu tinggi produk awet',
    desc: 'Proses sterilisasi dengan teknologi Retort menggunakan panas pada suhu tinggi...',
    img: 'https://ikitelurqu.com/asset_front/img/produksi_sterilisasi_retort.png'
  }
]
</script>

<style scoped>
.produksi {
  padding-top: 100px;
  padding-bottom: 100px;
}

.title_produksi {
  padding-bottom: 60px;
  text-align: center;
}

.title_produksi h3 {
  margin: 0px;
  color: var(--color-grey);
}

.title_produksi h2 {
  color: var(--color-blue);
  font-family: var(--font-baloo);
  font-weight: 700;
  margin: 0 auto;
}

.box_img_produksi {
  width: 100%;
  background-color: #FFF;
  box-shadow: -1px 8px 12px -4px rgba(105, 105, 105, 0.2);
  min-height: 450px;
}

.text_deskripsi_produksi {
  padding: 15px 15px 45px 15px;
}

.text_deskripsi_produksi h3 {
  font-family: var(--font-baloo);
  font-weight: 700;
  font-size: 20px;
  color: var(--color-grey);
  min-height: 60px;
}

.text_deskripsi_produksi span hr {
  border-top: 1px solid #5A5958;
  margin: 10px 0;
}

.text_deskripsi_produksi p {
  text-align: justify;
  font-family: var(--font-barlow);
  font-size: 14px;
}

.mb-30 { margin-bottom: 30px; }
</style>
