<template>
  <div class="moment-section section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">Praktis untuk Banyak Momen</h2>
        <p class="section-subtitle">
          Camilan Anak • Bekal Sekolah • Lauk Praktis • Teman Perjalanan
        </p>
      </div>

      <div class="row">
        <div class="col-md-6 mb-4" v-for="(item, i) in list" :key="i">
          <div class="moment-item">
            <div class="moment-img-wrapper">
              <img :src="item.img" :alt="item.title" class="moment-img" />
            </div>
            <div class="moment-content">
              <h3>{{ item.title }}</h3>
              <p>{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const list = [
  {
    title: "Camilan Anak tinggi protein",
    desc: "Solusi praktis makan enak yang bikin lahap sekaligus penuhi kebutuhan tinggi protein harianmu.",
    img: "/anak.png",
  },
  {
    title: "Teman Perjalanan",
    desc: "Solusi praktis anti repot saat di jalan, camilan lezat yang siap menemani setiap perjalananmu.",
    img: "/perjalanan.png", // Placeholder
  },
  {
    title: "Bekal Sekolah",
    desc: "Praktis maksimal! Tinggal buka kemasannya, hidangan lezat langsung siap dinikmati kapan pun kamu mau.",
    img: "/bekal.png", // Placeholder
  },
  {
    title: "Lauk Praktis",
    desc: "Solusi makan enak tanpa ribet! Cukup sajikan untuk nambah selera makan setiap hari.",
    img: "/lauk.png", // Placeholder
  },
];
</script>

<style scoped>
.moment-section {
  background-color: #fff;
  padding-top: 80px;
  padding-bottom: 80px;
}

.section-title {
  color: red; /* Red color as requested */
  font-family: var(--font-nunito);
  font-weight: 700;
  font-size: 36px;
  margin-bottom: 10px;
  margin-top: 0;
}

.section-subtitle {
  color: #666;
  font-family: var(--font-nunito);
  font-size: 16px;
  margin-bottom: 50px;
}

.moment-item {
  display: flex;
  align-items: center;
  gap: 20px;
  margin-bottom: 30px;
}

.moment-img-wrapper {
  flex-shrink: 0;
  width: 150px;
  height: 150px;
  border-radius: 50%;
  overflow: hidden;
  border: 5px solid #fff;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.moment-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.moment-content h3 {
  font-family: var(--font-nunito);
  font-weight: 700;
  font-size: 24px;
  margin-bottom: 10px;
  margin-top: 0;
  color: var(--heading-color);
}

.moment-content p {
  font-family: var(--font-nunito);
  font-size: 16px;
  line-height: 1.6;
  color: var(--text-color);
  margin-bottom: 0;
}

@media (max-width: 991px) {
  .moment-section {
    padding-top: 60px;
    padding-bottom: 60px;
  }

  .section-title {
    font-size: 28px;
  }
  
  .moment-item {
    flex-direction: column;
    text-align: center;
  }
  
  .moment-img-wrapper {
      margin: 0 auto 15px;
  }
}
</style>
