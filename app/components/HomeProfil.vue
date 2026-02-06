<template>
  <div class="profil">
    <div class="container">
       <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="img_profil_ikitelelurqu">
                <img src="https://ikitelurqu.com/asset_front/img/profil_ikitelurqu.png" class="img-responsive" alt="Image">
             </div>
             <!-- Pattern skipped as it might be complex to position perfectly without all assets locally, 
                  but we include the div for structure. -->
          </div>
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="deskripsi_profil_ikitelurqu">
                <h3>Oleh-oleh unik dan baru khas Jogja</h3>
                <h1>Asli dari Jogja untuk Indonesia</h1>
                <h2>Jogja terbuat dari rindu, pulang dan angkringan</h2>

                <div class="deskripsi_profil">
                   <p>Terdapat banyak tempat wisata yang menarik di Yogyakarta... (See full text in real content) ... Telur Puyuh rasa bacem khas Jogja.</p>
                   <p>Kini telah hadir telur puyuh bacem dalam kemasan yang dapat dinikmati kapanpun dan dimanapun...</p>
                </div>
                
                <div class="btn_outlet">
                   <a href="/outlet" class="btn btn-warning btn-lg">Lihat lokasi outlet</a>
                </div>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.profil {
  padding-top: 100px; /* Adjusted */
  padding-bottom: 100px;
  background-color: var(--color-blue-dark); /* Fallback */
  position: relative;
}

/* Original has background image */
/* .profil {
  background: url("../img/batik_iki_telurqu.png") no-repeat fixed;
  background-size: cover;
  background-blend-mode: multiply;
} */

.deskripsi_profil_ikitelurqu h3 {
  color: #FFF;
  font-family: var(--font-baloo); /* Regular */
  font-size: 24px;
}

.deskripsi_profil_ikitelurqu h1 {
  color: var(--color-gold);
  font-family: var(--font-baloo);
  font-weight: 800;
  font-size: 50px;
  margin: 0px;
  line-height: 1.2;
}

.deskripsi_profil_ikitelurqu h2 {
  color: var(--color-gold);
  font-family: var(--font-baloo); /* Regular */
  font-size: 25px;
  margin-bottom: 20px;
}

.deskripsi_profil {
  color: #FFF;
}

.deskripsi_profil p {
  text-align: justify;
  font-family: var(--font-barlow);
  padding-bottom: 20px;
}

.btn-warning {
  background-color: var(--color-gold);
  color: #000;
  border: none;
  font-family: var(--font-baloo);
  font-weight: 600;
  padding: 12px 30px;
  border-radius: 4px;
  font-size: 1.2rem;
  cursor: pointer;
  display: inline-block;
}
</style>
