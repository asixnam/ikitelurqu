<template>
  <div class="keunggulan-section section-padding">
    <div class="container">
      <div class="text-center mb-5">
        <h2 class="section-title">KEUNGGULAN IKI TELURQU</h2>
      </div>

      <div class="grid_list">
        <div class="row">
          <div
            class="col-md-6 col-lg-6 mb-4"
            v-for="(item, i) in list"
            :key="i"
          >
            <div class="box_keunggulan">
              <div class="icon-box">
                <img :src="item.img" :alt="item.title" class="icon-img" />
              </div>
              <div class="text_content">
                <h4>{{ item.title }}</h4>
                <p>{{ item.desc }}</p>
              </div>
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
    title: "Siap Santap",
    desc: "Buka kemasannya, nikmati kelezatan praktis yang langsung memanjakan lidahmu.",
    img: "/icon/ico_3.png",
  },
  {
    title: "Praktis Dibawa",
    desc: "Pilihan tepat untuk menemani sekolah, perjalanan, hingga rekreasi serumu.",
    img: "/icon/ico_2.png",
  },
  {
    title: "Masa Simpan Panjang",
    desc: "Kualitasnya terjaga, awet, serta sangat praktis disimpan di mana saja.",
    img: "/icon/ico_1.png",
  },
  {
    title: "Disukai Semua Usia",
    desc: "Pilihan lezat yang dicintai semua generasi, dari anak hingga dewasa.",
    img: "/icon/ico_4.png",
  },
];
</script>

<style scoped>
.keunggulan-section {
  background-color: #104196; /* Dark Blue similar to image */
  color: #fff;
  padding-top: 80px;
  padding-bottom: 80px;
}

.section-title {
  color: #fff;
  font-family: var(--font-nunito);
  font-weight: 700;
  font-size: 36px;
  margin-bottom: 50px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.box_keunggulan {
  display: flex;
  align-items: flex-start;
  gap: 20px;
  padding: 20px;
}

.icon-box {
  flex-shrink: 0;
  width: 80px;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon-img {
  width: 100%;
  height: auto;
  filter: brightness(0) invert(1); /* Make icons white */
}

.text_content h4 {
  color: var(--theme-color); /* Yellow/Orange */
  font-family: var(--font-nunito);
  font-weight: 700;
  font-size: 24px;
  margin-bottom: 10px;
}

.text_content p {
  color: #e0e0e0;
  font-family: var(--font-nunito);
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 0;
}

@media (max-width: 991px) {
  .keunggulan-section {
    padding-top: 60px;
    padding-bottom: 60px;
  }
  
  .section-title {
    font-size: 28px;
    margin-bottom: 30px;
  }

  .box_keunggulan {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
}
</style>
