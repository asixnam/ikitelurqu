<template>
  <div class="produksi section-padding bg-gray">
    <div class="container">
       <div class="section-title text-center mb-50">
          <span class="sub-title">Pengolahan modern</span>
          <h2>Diolah secara Modern & Otomatis</h2>
          <p class="section-desc">Proses produksi yang higienis dan modern menjamin kualitas terbaik untuk Anda.</p>
       </div>
       
       <div class="row">
          <!-- Video Section -->
          <div class="col-md-3 col-sm-6 mb-30">
             <div class="process-card video-card">
                <div class="video-wrapper">
                    <img src="https://ikitelurqu.com/asset_front/img/pabrik_ikitelurqu.mp4" alt="Video Placeholder" class="img-responsive video-thumb">
                    <div class="play-btn"><i class="glyphicon glyphicon-play"></i></div>
                </div>
             </div>
          </div>

          <!-- Process Steps -->
          <div class="col-md-3 col-sm-6 mb-30" v-for="(item, i) in steps" :key="i">
             <div class="process-card">
                <div class="card-img">
                   <img :src="item.img" class="img-responsive" alt="Image">
                </div>
                <div class="card-content">
                   <h3>{{ item.title }}</h3>
                   <div class="divider"></div>
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
    title: 'Rebus Otomatis',
    desc: 'Tahapan proses perebusan dengan suhu dan waktu yang tepat untuk kematangan sempurna.',
    img: 'https://ikitelurqu.com/asset_front/img/produksi_perebusan_otomatis.png'
  },
  {
    title: 'Kupas Otomatis',
    desc: 'Menggunakan mesin otomatis agar telur kupas lebih bersih, halus, dan higienis.',
    img: 'https://ikitelurqu.com/asset_front/img/produksi_kupas_otomatis.png'
  },
  {
    title: 'Sterilisasi Retort',
    desc: 'Pemanasan suhu tinggi membunuh bakteri sehingga produk awet tanpa pengawet.',
    img: 'https://ikitelurqu.com/asset_front/img/produksi_sterilisasi_retort.png'
  }
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
  display: block;
  margin-bottom: 5px;
}

.section-title h2 {
  font-size: 36px;
  color: var(--heading-color);
  font-weight: 700;
}

.section-desc {
  max-width: 600px;
  margin: 0 auto;
}

.process-card {
  background: #fff;
  border-radius: 6px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  transition: all 0.3s ease;
  height: 100%;
}

.process-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.1);
}

.card-img {
  text-align: center;
  overflow: hidden;
}

.card-img img {
  width: 100%;
  transition: transform 0.5s;
}

.process-card:hover .card-img img {
  transform: scale(1.05);
}

.card-content {
  padding: 25px;
}

.card-content h3 {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 15px;
  color: var(--heading-color);
}

.divider {
  width: 50px;
  height: 2px;
  background: var(--theme-color);
  margin-bottom: 15px;
}

.card-content p {
  font-size: 15px;
  color: #666;
  line-height: 1.6;
}

.video-wrapper {
  position: relative;
  height: 100%;
  min-height: 350px; /* Adjust as needed */
  background: #000;
  display: flex;
  align-items: center;
  justify-content: center;
}

.play-btn {
  width: 60px;
  height: 60px;
  background: rgba(255,255,255,0.8);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  z-index: 2;
  transition: all 0.3s;
}

.play-btn:hover {
  background: var(--theme-color);
  color: #fff;
}

.glyphicon-play {
  font-size: 24px;
}
</style>
