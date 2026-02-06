<template>
  <div class="latarbelakang">
    <div class="container">
       <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="img_keluarga_ikitelurqu">
                <img src="https://ikitelurqu.com/asset_front/img/keluarga_ikitelurqu.png" class="img-responsive" alt="Image">
             </div>
          </div>
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="deskripsi_latarbelakang">
                <h3>Alasan pilih Iki TelurQu</h3>
                <h2>Pilihan jajanan sehat untuk keluarga</h2>
                
                <div class="grid_list">
                   <div class="row">
                      <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6 mb-30" v-for="(item, i) in list" :key="i">
                         <div class="box_list_latarbelakang">
                            <div class="list_img">
                               <img :src="item.img" alt="">
                            </div>
                            <h4>{{ item.title }}</h4>
                            <p>{{ item.desc }}</p>
                         </div>
                      </div>
                   </div>
                </div>

                <div class="btn_keunggulan">
                   <a href="/profil" class="btn btn-danger">Keunggulan lainnya</a>
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
    title: 'Praktis & higienis',
    desc: 'Bahan kemasan Alumunium Retort tebal dan kedap udara untuk menjamin keamanan produk. Desain apik dan mudah dibawa kemanapun.',
    img: 'https://ikitelurqu.com/asset_front/img/ico_1.png'
  },
  {
    title: 'Enak & bergizi',
    desc: 'Terbuat dari 100% telur puyuh, Iki TelurQu tinggi protein. Hadir dengan rasa Bacem khas Jogja yang bikin kangen.',
    img: 'https://ikitelurqu.com/asset_front/img/ico_2.png'
  },
  {
    title: 'Tanpa pengawet',
    desc: 'Proses sterilisasi teknologi Retort memperpanjang masa simpan sampai 3 bulan (atau 1 tahun) tanpa bahan pengawet.',
    img: 'https://ikitelurqu.com/asset_front/img/ico_3.png'
  },
  {
    title: 'Penyimpanan mudah',
    desc: 'Dapat disimpan di suhu ruang, tidak perlu di kulkas. Mudah disusun dan tampilan menarik.',
    img: 'https://ikitelurqu.com/asset_front/img/ico_4.png'
  }
]
</script>

<style scoped>
.latarbelakang {
  padding-top: 120px;
  padding-bottom: 120px;
  background-color: var(--color-blue); /* #1643A0 */
}

.img_keluarga_ikitelurqu {
  padding-top: 60px;
}

.deskripsi_latarbelakang h3 {
  color: #FFF;
  font-size: 28px;
  margin-bottom: 10px;
}

.deskripsi_latarbelakang h2 {
  width: 80%; /* Adjusted from 55% for mobile/desktop balance */
  color: var(--color-gold); /* #FFD60A */
  font-family: var(--font-baloo);
  font-weight: 800;
  font-size: 40px;
  line-height: 1.2;
  margin-bottom: 40px;
}

.box_list_latarbelakang .list_img img {
  width: auto;
  height: 50px;
  margin-bottom: 15px;
}

.box_list_latarbelakang h4 {
  color: var(--color-gold);
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 10px;
}

.box_list_latarbelakang p {
  color: #FFF;
  text-align: justify;
  font-family: var(--font-barlow);
  font-size: 16px;
}

.btn_keunggulan {
  padding-top: 50px;
}

.btn-danger {
  background-color: var(--color-red);
  color: #fff;
  padding: 12px 30px;
  border: none;
  font-family: var(--font-baloo);
  font-size: 18px;
  cursor: pointer;
  border-radius: 5px;
}

.mb-30 {
  margin-bottom: 30px;
}

@media (max-width: 992px) {
  .deskripsi_latarbelakang h2 {
    width: 100%;
  }
}
</style>
