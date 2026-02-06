<template>
  <div class="profil">
    <div class="container">
       <div class="row display-flex">
          <!-- Left: Image with Pattern -->
          <div class="col-md-6 col-sm-12 image-section">
             <div class="image-wrapper">
                <div class=""></div>
                <!-- Using the premium box image which matches the 'Isi 5 pack' text in screenshot -->
                <img src="/profil.png" class="img-responsive main-img" alt="Iki TelurQu Box">
             </div>
          </div>
          
          <!-- Right: Text Content -->
          <div class="col-md-6 col-sm-12 text-section">
             <h4 class="sub-title">Iki TelurQu, camilan lezat & bergizi</h4>
             <h1 class="main-title">Pilihan Jajanan sehat untuk Keluarga</h1>
             
             <div class="deskripsi">
               <p>Iki TelurQu merupakan inovasi terbaru dari PT Malond Indo Perkasa, salah satu pionir industri puyuh di Indonesia. Iki TelurQu adalah telur puyuh RTE (ready-to-eat) yang diproses dengan teknologi sterilisasi retort dengan suhu tinggi untuk memastikan produk bebas bakteri dan jamur, masa simpan sampai dengan 3 bulan di suhu ruang tanpa bahan pengawet tambahan.</p>
               
               <p>Kemasan berbahan alumunium retort sesuai standar spesifikasi untuk olahan pangan sterilisasi, keamanan dan nilai gizi terjamin. Desain menarik, ukuran compact dan mudah disobek. Rangkaian proses produksi dilakukan di pabrik modern dan otomatis, mulai dari proses perebusan hingga pengupasan. Proses produksi telah menerapkan standar Program Manajemen Resiko (PMR-BPOM RI) yang beralamat di Jalan Wonosari Km. 22 Widoro Kulon, Kel. Bunder, Kec. Patuk, Kab. Gunungkidul. Produk ini telah mendapat sertifikat Halal BPJPH (Badan Penyelenggara Jaminan Produk Halal) dan BPOM Indonesia, sertifikat bebas borak dan formalin.</p>
               
               <p>Iki TelurQu hadir dengan rasa bacem khas Jogja, cocok dijadikan sebagai oleh-oleh khas yang unik dari Yogyakarta. Sebagai hampers atau bingkisan untuk kerabat tercinta. Iki TelurQu dapat dikonsumsi semua kalangan. Dengan kemasan compact dan praktis, cocok sebagai teman perjalanan, bekal dan camilan harian. Iki TelurQu tinggal sobek, langsung bisa dimakan.</p>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.profil {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: #fff;
  overflow: hidden;
}

.display-flex {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

/* Image Section Styling */
.image-section {
  position: relative;
  min-height: 600px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: -140px; /* Pull image upwards as requested */
}

.image-wrapper {
  position: relative;
  width: 100%;
  max-width: 650px; /* Increased from 500px */
  display: flex;
  justify-content: center;
}


.main-img {
  position: relative;
  z-index: 2;
  width: 100%; /* Increased from 80% */
  transform: rotate(-5deg); /* Slight tilt maybe? Screenshot looks straight/slightly angled 3D box */
  /* The image source itself might be 3D. */
}

/* Text Section Styling */
.text-section {
  padding-left: 0;
  margin-left: -10px; /* Pull text to the left as requested */
}

.sub-title {
  color: var(--color-grey);
  font-family: var(--font-barlow);
  font-size: 18px;
  margin-bottom: 10px;
  font-weight: 500;
}

.main-title {
  color: var(--color-blue);
  font-family: var(--font-baloo);
  font-weight: 800;
  font-size: 48px;
  line-height: 1.1;
  margin-top: 0;
  margin-bottom: 30px;
}

.deskripsi p {
  color: #666;
  font-family: var(--font-barlow);
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 20px;
  text-align: justify;
}

@media (max-width: 991px) {
  .display-flex {
    flex-direction: column;
  }
  .image-section {
    margin-bottom: 50px;
  }
  .blue-circle-bg {
    width: 300px;
    height: 300px;
    padding-bottom: 0;
  }
  .main-title {
    font-size: 32px;
  }
  .text-section {
    margin-left: 0;
    padding-left: 15px; /* Restore bootstrap default padding on mobile */
  }
}
</style>
