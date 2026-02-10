<template>
  <div class="tips-section section-padding">
    <div class="container">
      <div class="text-center mb-50">
        <h2 class="section-title">Tips Untuk Menikmati Iki TelurQu</h2>
        <div class="divider"></div>
      </div>

      <div class="row">
        <div class="col-md-6 mb-40" v-for="(item, i) in tips" :key="i">
          <div class="tips-item">
            <div class="tips-img">
              <img :src="item.img" :alt="item.title" class="img-responsive">
            </div>
            <div class="tips-content">
              <h4>{{ item.title }}</h4>
              <p>{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const tips = [
  {
    title: 'Langsung Santap (Ready to Eat)',
    desc: 'Kenikmatan tanpa drama, tinggal sobek aja.',
    img: '/sobek.png' // Placeholder for "hand holding package"
  },
  {
    title: 'Menemanimu saat Makan',
    desc: 'Jangan biarkan nasi kesepian. Pasangkan dengan ini, biar jadi couple goals di piringmu!',
    img: '/nasi.png' // Placeholder for "rice and eggs"
  },
  {
    title: 'Panaskan Beserta Kemasan',
    desc: 'Gak pakai lama! Cukup 3 menit, kehangatannya langsung bikin nagih.',
    img: '/masak.png' // Placeholder for "boiling pot"
  },
  {
    title: 'Buat Stok lauk Sarapan',
    desc: 'Gak Usah takut kehabisan kamu bisa stok, dan simpan hindari sinar matahari secara langsung',
    img: '/box.png' // Placeholder for "box" 
  }
]
</script>

<style scoped>
.tips-section {
  padding-top: 80px;
  padding-bottom: 80px;
  background-color: #fff;
}

.section-title {
  color: red;
  font-family: var(--font-nunito);
  font-weight: 800;
  font-size: 36px;
  margin-bottom: 20px;
  margin-top: 0;
  text-transform: uppercase;
  color: #d32f2f;
}

.divider {
  height: 2px;
  background-color: #d32f2f;
  width: 100px; /* Short red bar */
  margin: 20px auto 50px;
}

.tips-item {
  display: flex;
  align-items: center; /* Center vertically against text */
  gap: 15px; /* Tighter gap */
  padding: 0;
  transition: all 0.3s ease;
}

.tips-item:hover {
  transform: translateY(-5px);
}

.tips-img {
  flex: 0 0 140px; /* Slightly smaller */
  max-width: 140px;
  overflow: hidden;
}

.tips-img img {
  width: 100%;
  height: auto;
  display: block;
  object-fit: contain;
  transition: transform 0.5s ease;
}

.tips-item:hover .tips-img img {
   transform: scale(1.05);
}

.tips-content {
  flex: 1;
}

.tips-content h4 {
  font-family: var(--font-nunito);
  font-weight: 700;
  font-size: 18px; /* Reduced from 20px */
  color: #333;
  margin-top: 0;
  margin-bottom: 5px;
  line-height: 1.3;
}

.tips-content p {
  font-family: var(--font-nunito);
  font-size: 15px;
  color: #666;
  line-height: 1.6;
  margin-bottom: 0;
}

.mb-50 { margin-bottom: 50px; }
.mb-40 { margin-bottom: 40px; }

@media (max-width: 767px) {
  .tips-item {
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin-bottom: 30px;
    padding: 15px;
    border: 1px solid #f9f9f9; /* Subtle border on mobile */
  }
  
  .tips-img {
    margin-bottom: 15px;
    width: 100px; /* Smaller on mobile */
    max-width: 100px;
  }
  
  .section-title {
     font-size: 28px;
  }
  
  .tips-content h4 {
    font-size: 18px;
  }
}
</style>
