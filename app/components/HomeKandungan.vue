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
                <img src="/anak_ikitelurqu.png" class="img-responsive" alt="Image">
             </div>
          </div>
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="deskripsi_kandungan">
                <p>Salah satu manfaat telur puyuh yang jarang diketahui adalah mencegah stunting pada anak. Stunting adalah kondisi di mana pertumbuhan anak terhambat akibat kurang gizi kronis. Stunting dapat menyebabkan gangguan kognitif, fisik, dan imunitas pada anak. Telur puyuh dapat mencegah stunting karena kandungan protein dan lemaknya yang cukup tinggi. Protein dan lemak dapat membantu pertumbuhan sel dan jaringan tubuh, serta memenuhi kebutuhan energi anak.</p>
                <p>Iki TelurQu alternatif jajanan sehat dan mengenyangkan, terbuat dari 100% telur puyuh pilihan, tinggi zat besi dan protein yang dibutuhkan anak-anak di masa pertumbuhan. Iki TelurQu juga dapat dijadikan lauk untuk bekal makan siang di sekolah.</p>

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
  background-color: var(--color-bg-light); /* Keep light bg or use #f9f9f9 */
}

.title_kandungan {
  padding-bottom: 60px;
  text-align: center;
}

.title_kandungan h3 {
  margin: 0px 0 10px;
  color: var(--theme-color); /* Orange */
  font-family: var(--font-josefin);
  font-size: 20px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.title_kandungan h2 {
  margin: 0px;
  color: var(--heading-color); /* Dark Blue */
  font-family: var(--font-poppins);
  font-weight: 700;
  font-size: 40px;
}

.deskripsi_kandungan p {
  text-align: justify;
  font-family: var(--font-poppins);
  padding-bottom: 15px;
  font-size: 15px;
  line-height: 1.8;
  color: var(--text-color);
  font-weight: 400;
}

.deskripsi_kandungan h4 {
  color: var(--theme-color); /* Red -> Orange/Theme */
  font-family: var(--font-poppins);
  font-weight: 600;
  font-size: 20px;
  margin-top: 20px;
  margin-bottom: 20px;
  line-height: 1.4;
}

.list_kandungan ul {
  padding-left: 0;
  list-style: none;
}

.list_kandungan ul li {
  color: #FFF;
  margin-top: 15px;
  font-size: 16px;
  font-family: var(--font-poppins);
  font-weight: 500;
}

.custom_text_kandungan {
  background-color: var(--theme-color); /* Red -> Orange */
  padding: 8px 15px;
  border-radius: 50px; /* Pill shape */
  display: inline-block;
  box-shadow: 0 4px 10px rgba(255, 86, 0, 0.2);
}

.normal_text {
  font-weight: 400;
  font-size: 0.9em;
  opacity: 0.9;
}

@media (max-width: 991px) {
  .kandungan {
    padding-top: 60px;
    padding-bottom: 60px;
  }
  .title_kandungan h2 {
    font-size: 28px;
  }
  .title_kandungan h3 {
    font-size: 16px;
  }
  .img_anak_anak {
    margin-bottom: 30px;
    text-align: center;
  }
}
</style>
