<template>
  <div class="varian-section section-padding">
    <div class="container">
      <div class="text-center mb-50">
        <h2 class="section-title">EMPAT VARIAN FAVORIT KELUARGA</h2>
        <p class="section-subtitle">
          Dari Pedas Nampol Sampai Manis Legit, Semuanya Ada.
        </p>
      </div>

      <div class="row">
        <div
          class="col-md-3 col-sm-6 mb-30"
          v-for="(item, i) in list"
          :key="i"
        >
          <div class="varian-item">
             <div class="varian-card" :style="{ backgroundColor: item.color }">
                <div class="varian-img-wrapper">
                  <img :src="item.img" :alt="item.title" class="varian-img" />
                </div>
             </div>
             <div class="varian-info text-center">
                <h4>{{ item.title }}</h4>
                <p>{{ item.desc }}</p>
             </div>
          </div>
        </div>
      </div>

      <div class="text-center mt-30">
        <NuxtLink to="/varian" class="btn-theme">Lihat Semua Varian</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const list = [
  {
    title: "Bacem",
    desc: "Manisnya pas",
    img: "/bacem.png", // Placeholder
    color: "#ba5a06", // Brown
  },
  {
    title: "Pedas",
    desc: "Pedasnya terasa",
    img: "/pedas.png", // Placeholder
    color: "#ff0000", // Red
  },
  {
    title: "Kuning",
    desc: "Gurihnya Nagih",
    img: "/kuning.png", // Placeholder
    color: "#ffc107", // Yellow
  },
  {
    title: "Opor",
    desc: "Bikin Kangen",
    img: "/opor.png", // Placeholder
    color: "#f57c00", // Orange
  },
];
</script>

<style scoped>
.varian-section {
  background-color: #fff;
  padding-top: 80px;
  padding-bottom: 80px;
}

.mb-50 {
    margin-bottom: 50px;
}

.mb-30 {
    margin-bottom: 30px;
}

.mt-30 {
    margin-top: 30px;
}

.section-title {
  color: #ff0000; /* Red */
  font-family: var(--font-nunito);
  font-weight: 800;
  font-size: 32px;
  margin-bottom: 10px;
  margin-top: 0;
  text-transform: uppercase;
}

.section-subtitle {
  color: #555;
  font-family: var(--font-nunito);
  font-size: 18px;
  margin-bottom: 0px;
}

.varian-item {
    transition: transform 0.3s ease;
}

.varian-item:hover {
    transform: translateY(-10px);
}

.varian-card {
  border-radius: 20px;
  padding: 20px;
  height: 280px; /* Slightly taller */
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
  position: relative;
  overflow: hidden;
  box-shadow: 0 10px 20px rgba(0,0,0,0.05); /* Subtle shadow */
}

.varian-img-wrapper {
  width: 100%;
  text-align: center;
}

.varian-img {
  max-width: 85%;
  max-height: 220px;
  object-fit: contain;
  filter: drop-shadow(0 5px 10px rgba(0,0,0,0.2));
  transform: translateX(-15px) rotate(-10deg); /* Shift left and rotate */
  transition: transform 0.3s ease;
}

.varian-item:hover .varian-img {
    transform: translateX(-5px) rotate(0deg) scale(1.05); /* Reset on hover for effect */
}

.varian-info h4 {
  color: #d32f2f; /* Dark Red */
  font-family: var(--font-nunito);
  font-weight: 800;
  font-size: 22px;
  margin-bottom: 5px;
}

.varian-info p {
  color: #333;
  font-family: var(--font-nunito);
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 0px;
}

/* Using global .btn-theme from main.css, ensuring specific overrides if needed */
.btn-theme {
    padding: 15px 40px;
    font-size: 16px;
    border-radius: 50px; /* Pill shape */
}

@media (max-width: 991px) {
  .section-title {
    font-size: 24px;
  }
}
</style>
