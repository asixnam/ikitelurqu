<template>
  <div class="header_page section-padding">
    <div class="container">
      <div class="row align-items-center">
        <!-- Text Left -->
        <div class="col-md-6 col-lg-6 mb-50">
           <div class="header_text">
              <span class="sub-title">Pertama di Indonesia</span>
              <h1>Iki TelurQu</h1>
              <h2>Telur puyuh siap santap</h2>

              <div class="header_deskripsi">
                 <p>Iki TelurQu adalah telur puyuh RTE (ready-to-eat) yang diproses dengan teknologi retort sehingga bebas bakteri dan jamur. Produk kami tahan 3 bulan di suhu ruang tanpa bahan pengawet tambahan.</p>
                 <p class="hidden-xs">Terbuat dari 100% telur puyuh pilihan dan diolah dengan bumbu terbaik untuk menciptakan cita rasa yang lezat. Cocok dikonsumsi untuk anak-anak dalam masa pertumbuhan.</p>
              </div>

              <div class="button_header mt-30">
                 <NuxtLink to="/profil" class="btn-theme">Tentang Iki TelurQu</NuxtLink>
              </div>
           </div>
        </div>

        <!-- Image Right -->
        <div class="col-md-6 col-lg-6">
           <div class="header_img text-center">
              <img src="/header.png" class="img-responsive hero-img" alt="Iki TelurQu Hero Image">
           </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header_page {
  background: #f7f7fd url('/bg-hero.png') no-repeat right top; /* Optional background pattern */
  background-size: contain; 
}

/* Vertical Align Helper for Bootstrap 3 if flex not available, 
   but we added align-items-center which needs flex. 
   If bootstrap 3, we might need manual css for flex 
*/
.row.align-items-center {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.sub-title {
  color: var(--theme-color);
  font-family: var(--font-poppins);
  font-weight: 500;
  font-size: 18px;
  display: block;
  margin-bottom: 10px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.header_text h1 {
  font-family: var(--font-poppins);
  font-weight: 700;
  font-size: 60px;
  line-height: 1.1;
  color: var(--heading-color);
  margin-bottom: 10px;
}

.header_text h2 {
  font-family: var(--font-josefin);
  font-weight: 400;
  font-size: 32px;
  color: var(--text-color);
  margin-bottom: 25px;
}

.header_deskripsi p {
  color: var(--text-color);
  font-size: 16px;
  line-height: 28px;
  margin-bottom: 15px;
}

.hero-img {
  max-width: 100%;
  height: auto;
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
	0% { transform: translatey(0px); }
	50% { transform: translatey(-20px); }
	100% { transform: translatey(0px); }
}

@media (max-width: 991px) {
  .header_page {
    text-align: center;
    padding-top: 100px; /* Space for fixed header */
  }
  
  .header_text {
    margin-bottom: 40px;
  }

  .header_text h1 {
    font-size: 42px;
  }

  .header_text h2 {
    font-size: 24px;
  }
  
  .row.align-items-center {
    display: block; /* Stack on mobile */
  }

  .button_header {
    margin-bottom: 30px;
  }
}
</style>
