<template>
  <div class="home-jogja">
    <div class="container">
       <div class="row display-flex">
          <!-- Left: Images (Polaroid Stack) -->
          <div class="col-md-6 col-sm-12 image-cluster">
             <!-- Main large polaroid -->
             <div class="polaroid main-polaroid">
                <div class="img-box">
                    <!-- Placeholder or specific image text. Screenshot has 'Jogja terbuat dari rindu...' text ON the image. 
                         I'll use a placeholder or the profil image if suitable. -->
                    <img src="/profil_ikitelurqu.png" class="img-responsive" alt="Jogja">
                </div>
             </div>
             
             <!-- Line Art Decoration at bottom -->
             <div class="image">
                 <div class="jogja">
                    <img src="/jogja.png" class="img-responsive" alt="Jogja">
                 </div>
             </div>
          </div>
          
          <!-- Right: Text Content -->
          <div class="col-md-6 col-sm-12 text-content">
             <h4 class="sub-title">Oleh-oleh unik dan baru khas Jogja</h4>
             <h1 class="main-title">Asli dari Jogja <br>untuk Indonesia</h1>
             <h3 class="tagline">Jogja terbuat dari rindu, pulang dan angkringan</h3>
             
             <div class="description">
                 <p>Terdapat banyak tempat wisata yang menarik di Yogyakarta, mulai dari wisata sejarah, wisata alam, hingga wisata kuliner. Angkringan salah satu kuliner khas Yogyakarta yang terkenal dan menjadi daya tarik wisata di Yogyakarta. Tempat yang asyik untuk berdiskusi dan menikmati suasana malam Jogja.</p>
                 
                 <p>Kini telah hadir telur puyuh bacem dalam kemasan yang dapat dinikmati kapanpun dan dimanapun. Iki TelurQu hadir sebagai obat kangen bagi kamu yang ingin menikmati telur puyuh khas Jogja. Dikemas secara apik dan modern, awet hingga tiga bulan di suhu ruang.</p>
                 
                 <p>Oleh-oleh unik baru yang bikin liburan kamu semakin berkesan, dapat dibeli di toko oleh-oleh, supermarket, swalayan dan toko kelontong yang telah tersebar di lebih dari 400 titik outlet di wilayah Jogja dan sekitarnya.</p>
             </div>
             
             <div class="action-btn">
                <a href="/outlet" class="btn btn-warning">Lihat lokasi outlet</a>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.home-jogja {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: #3b6e05; /* Deep Green from screenshot */
  /* Fallback or if pattern exists: */
  background-image: url('/pettern.png'); 
  position: relative;
  overflow: hidden;
  color: #fff;
}

/* Background Pattern overlay simulation if needed */
.home-jogja::before {
  content: "";
  position: absolute;
  top:0; left:0; right:0; bottom:0;
  background-image: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
  background-size: 10px 10px;
  opacity: 0.3;
  pointer-events: none;
}

.display-flex {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
}

/* Image Cluster */
.image-cluster {
  position: relative;
  min-height: 500px;
}

.polaroid {
  padding: 10px;
  padding-bottom: 30px; /* Polaroid style bottom */
  display: inline-block;
  transform: rotate(-3deg);
  transition: transform 0.3s;
}

.polaroid:hover {
  transform: rotate(0deg) scale(1.05);
  z-index: 10;
}

.main-polaroid {
  width: 80%; /* Increased from 70% */
  z-index: 2;
  position: absolute;
  top: 0;
  left: 5%; /* Adjusted from 10% to center better with wider width */
}

.small-polaroids-wrapper {
  position: absolute;
  bottom: 50px;
  left: 0;
  width: 100%;
}

.small-polaroid {
  width: 40%;
  position: absolute;
}

.p1 {
  left: 0;
  bottom: 0;
  transform: rotate(5deg);
  z-index: 3;
}

.p2 {
  right: 10px;
  bottom: 20px;
  transform: rotate(-5deg);
  z-index: 3;
}

/* Decoration Line / Jogja Image */
.image {
  position: absolute;
  bottom: -50px;
  left: 30px;
  width: 100%;
  z-index: 1; /* Behind polaroid if overlapping, or just bottom layer */
}

.jogja img {
  width: 70%;
  display: block;
}

/* Text Content */
.sub-title {
  font-family: var(--font-baloo);
  font-size: 20px;
  font-weight: 500;
  color: #fff;
  margin-bottom: 5px;
}

.main-title {
  font-family: var(--font-baloo);
  font-size: 50px;
  font-weight: 800;
  color: var(--color-gold); /* Yellow */
  line-height: 1.1;
  margin-top: 5px;
  margin-bottom: 20px;
}

.tagline {
  font-family: var(--font-baloo);
  font-size: 24px;
  color: #a4ce4e; /* Light Greenish Yellow from screenshot */
  font-weight: 600;
  margin-bottom: 25px;
}

.description p {
  font-family: var(--font-barlow);
  font-size: 14px;
  line-height: 1.6;
  margin-bottom: 15px;
  color: #e0e0e0;
  text-align: justify;
}

.btn-warning {
  background-color: var(--color-gold);
  color: #3b6e05; /* Green text matching bg */
  font-family: var(--font-baloo);
  font-weight: 700;
  padding: 10px 30px;
  border: none;
  border-radius: 5px;
  margin-top: 10px;
}

@media (max-width: 991px) {
  .display-flex {
    flex-direction: column-reverse; /* Text first on mobile? Or image? Screenshot implies desktop. Let's stack naturally. */
  }
  .image-cluster {
    margin-bottom: 50px;
    min-height: 400px;
  }
  .main-title {
    font-size: 36px;
  }
}
</style>
