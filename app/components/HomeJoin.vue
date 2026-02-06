<template>
  <div class="contact_agen">
     <div class="container">
        <div class="row">
           <div class="col-xs-12 col-sm-12 col-md-4 col-lg-4">
              <div class="img_aktor_agen">
                 <img src="https://ikitelurqu.com/asset_front/img/agen_ikitelurqu.png" class="img-responsive" alt="Image">
              </div>
           </div>
           <div class="col-xs-12 col-sm-12 col-md-4 col-lg-4">
              <div class="box_deskripsi_agen">
                 <h3>Penawaran spesial</h3>
                 <h2>Jadilah agen berikutnya</h2>
                 <h4>Dapatkan keuntungan menarik dengan bergabung menjadi agen dan reseller Iki TelurQu. Terbuka untuk semua daerah di seluruh Indonesia</h4>
              </div>
           </div>
           <div class="col-xs-12 col-sm-12 col-md-4 col-lg-4">
              <div class="btn_join_agen">
                 <a href="https://api.whatsapp.com/send?phone=6282190000716&text=Hallo%20Admin%20IkiTelurQu%20Saya%20Mau%20Bergabung%20Menjadi%20Agen%20Distributor" target="_blank" class="btn btn-success btn-lg">Gabung sekarang</a>
                 <p>Atau hubungi admin kami : <br> Pukul 08:00 - 16:00 WIB</p>
              </div>
           </div>
        </div>
     </div>
  </div>
</template>

<style scoped>
.contact_agen {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: #FFF;
}

.img_aktor_agen {
  text-align: center;
}

.img_aktor_agen img {
  display: inline-block;
}

.box_deskripsi_agen h3 { color: var(--color-grey); margin-top: 0; }
.box_deskripsi_agen h2 { 
  color: var(--color-blue); 
  font-family: var(--font-baloo); 
  font-weight: 700; 
  font-size: 36px;
  margin: 10px 0;
}
.box_deskripsi_agen h4 { 
  color: var(--color-grey); 
  line-height: 1.5;
  font-weight: 400;
}

.btn_join_agen {
  text-align: center;
  padding-top: 40px;
}

.btn-success {
  background-color: var(--color-green);
  border: none;
  font-family: var(--font-baloo);
  font-size: 20px;
  padding: 15px 40px;
  border-radius: 50px;
  margin-bottom: 20px;
}

.btn_join_agen p {
  color: var(--color-grey);
}

@media (max-width: 992px) {
  .btn_join_agen { padding-top: 0; }
  .box_deskripsi_agen { text-align: center; margin-bottom: 30px; }
}
</style>
