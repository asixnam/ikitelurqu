<template>
  <div class="kandungan">
    <div class="container">
       <div class="title_kandungan">
          <h3>Cegah Stunting Itu Penting</h3>
          <h2>Cegah Stunting Dengan Telur Puyuh!</h2>
       </div>

       <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="img_anak_anak">
                <img src="https://ikitelurqu.com/asset_front/img/anak_ikitelurqu.png" class="img-responsive" alt="Image">
             </div>
          </div>
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="deskripsi_kandungan">
                <p>Salah satu manfaat telur puyuh yang jarang diketahui adalah mencegah stunting pada anak...</p>
                <p>Iki TelurQu alternatif jajanan sehat dan mengenyangkan...</p>

                <h4>Kandungan gizi telur puyuh lebih tinggi dibanding telur ayam ras*</h4>
                <div class="list_kandungan">
                   <ul>
                      <li><span class="custom_text_kandungan">Zat besi 3,65 mg <span class="normal_text">(3X telur ayam)</span></span></li>
                      <li><span class="custom_text_kandungan">Kalsium 64 mg</span></li>
                      <li><span class="custom_text_kandungan">Protein 13,1 g</span></li>
                   </ul>
                   <p>*Takaran saji per 100 gram</p>
                </div>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.kandungan {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: var(--color-bg-light); /* #F5F5FA */
}

.title_kandungan {
  padding-bottom: 60px;
  text-align: center;
}

.title_kandungan h3 {
  margin: 0px;
  color: var(--color-grey);
}

.title_kandungan h2 {
  margin: 0px;
  color: var(--color-blue);
  font-family: var(--font-baloo);
  font-weight: 700;
  font-size: 40px;
}

.deskripsi_kandungan p {
  text-align: justify;
  font-family: var(--font-barlow);
  padding-bottom: 20px;
  font-size: 18px;
}

.deskripsi_kandungan h4 {
  color: var(--color-red);
  font-family: var(--font-baloo);
  font-weight: 700;
  font-size: 24px;
}

.list_kandungan ul li {
  color: #FFF;
  margin-top: 10px;
  font-size: 24px;
  font-family: var(--font-baloo);
  font-weight: 600;
}

.custom_text_kandungan {
  background-color: var(--color-red);
  padding: 5px 15px;
  border-radius: 30px; /* Approximation */
  display: inline-block;
}

.normal_text {
  font-weight: 400;
  font-size: 0.9em;
}
</style>
