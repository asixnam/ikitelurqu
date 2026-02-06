<template>
  <div class="header_page">
    <div class="container">
      <div class="row header-content">
        <!-- Image Left (Desktop) or Top (Mobile) - original has col-md-6 order? 
             Actually original source: 
             col-md-6 img (left)
             col-md-6 text (right)
        -->
        <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
           <div class="header_img">
              <!-- Using original image URL if available or placeholder -->
              <img src="/header.png" class="img-responsive" alt="Image">
           </div>
        </div>

        <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
           <div class="header_text">
              <h3>Pertama di Indonesia</h3>
              <h1>Iki TelurQu</h1>
              <h2>Telur puyuh siap santap</h2>

              <div class="header_deskripsi">
                 <p>Iki TelurQu adalah telur puyuh RTE (ready-to-eat) yang diproses dengan teknologi retort sehingga bebas bakteri dan jamur. Produk kami tahan 1 tahun di suhu ruang tanpa bahan pengawet tambahan. Terbuat dari 100% telur puyuh pilihan dan diolah dengan bumbu terbaik untuk menciptakan cita rasa yang lezat.</p>
                 <p>Cocok dikonsumsi untuk anak-anak dalam masa pertumbuhan sebagai sumber protein bergizi yang lezat dan higienis. Cocok juga untuk oleh-oleh dari jogja karena kemasannya premium dan rasanya enak banget, yang pasti dijamin higenisnya.</p>
              </div>

              <div class="button_header">
                 <a href="/profil" class="btn btn-danger btn-lg">Tentang Iki TelurQu</a>
              </div>
           </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header_page {
  /* Padding top to account for absolute header if needed, but original likely had separate spacing */
  padding-top: 110px; 
}

.header_img img {
  width: 100%;
}

.header_text {
  text-align: left;
}

.header_text h3 {
  margin: 0px;
  font-family: var(--font-baloo); /* Regular */
  font-weight: 400;
  font-size: 28px;
  color: var(--color-grey);
}

.header_text h1 {
  margin: 0px;
  color: var(--color-blue); /* #1643A0 */
  font-family: var(--font-baloo);
  font-weight: 800; /* ExtraBold */
  font-size: 65px;
  line-height: 1.1;
}

.header_text h2 {
  margin: 0px;
  font-family: var(--font-baloo);
  font-weight: 500; /* Medium */
  font-size: 40px;
  color: var(--color-grey);
}

.header_deskripsi p {
  font-family: var(--font-barlow);
  font-size: 20px;
  text-align: justify;
  padding-top: 20px;
  color: var(--color-grey);
}

.button_header {
  padding-top: 10px;
}

.btn-danger {
  background-color: var(--color-red);
  color: white;
  padding: 10px 30px;
  border-radius: 4px;
  font-size: 1.2rem;
  font-family: var(--font-baloo);
  border: none;
  cursor: pointer;
  display: inline-block;
}

.btn-danger:hover {
  background-color: var(--color-red-bright);
}

@media (max-width: 992px) {
  .header_page {
    text-align: center;
  }
  .header_text {
    margin-top: 30px;
    text-align: center;
  }
  .header_text h1 {
    font-size: 48px;
  }
}
</style>
