<template>
  <div class="header_page">
    <div class="container">
      <div class="row align-items-center">
        <!-- Text Left -->
        <div class="col-md-6 col-lg-6 mb-50">
          <div class="header_text">
            <span class="sub-title">IKI TELURQU</span>
            <h1 class="hero-title">Telur Puyuh Siap Santap untuk Keluarga Aktif</h1>

            <div class="header_deskripsi">
              <p>
                Solusi Praktis Setiap Hari. Lezat dan praktis, produk ini adalah
                pilihan tepat untuk bekal kantor, camilan santai, hingga lauk
                harian keluarga. Cukup sajikan dalam sekejap untuk menikmati
                rasa autentik yang memanjakan lidah di setiap suasana sibukmu.
              </p>
            </div>

            <div class="button_header mt-4">
              <NuxtLink to="https://shopee.co.id/ikienak" class="btn-theme">Beli Sekarang</NuxtLink>
              <NuxtLink to="/varian" class="btn-border">Pilih Varian</NuxtLink>
            </div>
          </div>
        </div>

        <!-- Image Right -->
        <div class="col-md-6 col-lg-6">
          <div class="header_img text-center">
            <img
              src="/hero.png"
              class="img-fluid hero-img"
              alt="Iki TelurQu Keluarga"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header_page {
  background: var(--bg-gray); /* Use variable for consistency */
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
  padding-top: 60px;
  padding-bottom: 1px;
}

.sub-title {
  color: var(--theme-color);
  font-family: var(--font-poppins);
  font-weight: 600;
  font-size: 16px; /* Adjusted size */
  text-transform: uppercase; /* Uppercase for subtitle style */
  letter-spacing: 2px; /* Added letter spacing */
  display: block;
  margin-top: 80px;
  margin-bottom: 10px;
}

.hero-title {
  font-family: var(--font-poppins);
  font-weight: 700;
  font-size: 48px;
  line-height: 1.3;
  color: var(--text-color);
  margin-bottom: 25px;
}

.header_deskripsi p {
  color: var(--text-color);
  font-size: 18px; /* Slightly larger for readability */
  line-height: 1.8;
  margin-bottom: 35px;
  opacity: 0.9;
}

.button_header {
  display: flex;
  align-items: center;
  gap: 20px;
}

.hero-img {
  max-width: 100%;
  height: auto;
  margin-top: -50px; /* Pull image up */
  position: relative;
  z-index: 1;
  animation: float 6s ease-in-out infinite;
  filter: drop-shadow(0 10px 15px rgba(0, 0, 0, 0.1)); /* Add depth */
}

/* Animations */
@keyframes float {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
  100% {
    transform: translateY(0px);
  }
}

/* Responsive */
@media (max-width: 991px) {
  .header_page {
    text-align: center;
    padding-top: 60px;
    padding-bottom: 60px;
  }

  .hero-title {
    font-size: 32px;
  }

  .header_deskripsi p {
    font-size: 16px;
  }

  .button_header {
    justify-content: center;
    margin-bottom: 40px;
  }
  
  .hero-img {
      max-width: 80%; /* Smaller image on mobile */
  }
}
</style>
