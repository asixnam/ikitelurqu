<template>
  <div class="slide_momen">
     <div class="container">
        <div id="carousel-id" class="carousel slide" data-ride="carousel">
           <div class="carousel_buttom">
              <ol class="carousel-indicators carousel-indicators-custom">
                 <li data-target="#carousel-id" data-slide-to="0" class="active"></li>
                 <li data-target="#carousel-id" data-slide-to="1"></li>
                 <li data-target="#carousel-id" data-slide-to="2"></li>
                 <li data-target="#carousel-id" data-slide-to="3"></li>
              </ol>
           </div>
           
           <div class="carousel-inner">
              <div class="item active">
                 <div class="row">
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="img_carousel">
                          <img src="https://ikitelurqu.com/asset_front/img/slide/slide_lg_1.png" alt="">
                       </div>
                       <div class="box_text_img">
                          <h3>Iki TelurQu tinggi Kolin</h3>
                       </div>
                    </div>
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="slide_content">
                          <h3>Momen Iki TelurQu</h3>
                          <h1>Camilan penambah semangat belajar</h1>
                          <p>Kandungan Kolin dalam telur puyuh dapat membantu :</p>
                          <ul>
                             <li>Mengoptimalkan perkembangan otak anak</li>
                             <li>Meningkatkan daya pikir</li>
                             <li>Meningkatkan fokus anak dan konsentrasi</li>
                             <li>Meningkatkan daya ingat</li>
                          </ul>
                       </div>
                    </div>
                 </div>
              </div>

              <div class="item">
                 <div class="row">
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="img_carousel">
                          <img src="https://ikitelurqu.com/asset_front/img/slide/slide_lg_2.png" alt="">
                       </div>
                       <div class="box_text_img">
                          <h3>Iki TelurQu tinggi Protein</h3>
                       </div>
                    </div>
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="slide_content">
                          <h3>Momen Iki TelurQu</h3>
                          <h1>Asupan golden hour setelah olahraga</h1>
                          <p>Iki TelurQu asupan tepat setelah berolahraga untuk mengembalikan energi dan stamina tubuh yang telah terpakai. 1 bungkus Iki TelurQu (4 butir) mengandung :</p>
                          <ul>
                             <li>5g protein</li>
                             <li>80 kkal energi total</li>
                          </ul>
                       </div>
                    </div>
                 </div>
              </div>

              <div class="item">
                 <div class="row">
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="img_carousel">
                          <img src="https://ikitelurqu.com/asset_front/img/slide/slide_lg_3.png" alt="">
                       </div>
                       <div class="box_text_img">
                          <h3>Tinggi Lemak, Protein, Kabohidrat</h3>
                       </div>
                    </div>
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="slide_content">
                          <h3>Momen Iki TelurQu</h3>
                          <h1>Bekal di sekolah dan bekal kerja</h1>
                          <p>Iki TelurQu memiliki kandungan nutrisi seimbang dan sehat, lauk untuk bekal makan siang yang dapat :</p>
                          <ul>
                             <li>Meningkatkan konsentrasi kerja dan belajar</li>
                             <li>Menjaga tetap bertenaga selama di sekolah</li>
                             <li>Memastikan anak & keluarga tetap sehat.</li>
                          </ul>
                       </div>
                    </div>
                 </div>
              </div>

              <div class="item">
                 <div class="row">
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="img_carousel">
                          <img src="https://ikitelurqu.com/asset_front/img/slide/slide_lg_4.png" alt="">
                       </div>
                       <div class="box_text_img">
                          <h3>Kemasan Compact & Awet</h3>
                       </div>
                    </div>
                    <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
                       <div class="slide_content">
                          <h3>Momen Iki TelurQu</h3>
                          <h1>Camilan saat santai & teman perjalanan</h1>
                          <p>Iki TelurQu hadir dengan kemasan compact, mudah disobek, praktis sudah matang tinggal makan. Awet sampai 3 bulan di suhu ruang.</p>
                       </div>
                    </div>
                 </div>
              </div>
           </div>
           
           <a class="left carousel-control" href="#carousel-id" data-slide="prev"><span class="glyphicon glyphicon-chevron-left"></span></a>
           <a class="right carousel-control" href="#carousel-id" data-slide="next"><span class="glyphicon glyphicon-chevron-right"></span></a>
        </div>
     </div>
  </div>
</template>

<style scoped>
.slide_momen {
  padding-top: 100px;
  padding-bottom: 100px;
}

.slide_content h3 {
  color: var(--color-grey);
  margin-top: 0;
}

.slide_content h1 {
  color: var(--color-blue);
  font-family: var(--font-baloo);
  font-weight: 800;
  font-size: 40px;
  line-height: 1.2;
}

.slide_content ul {
  padding-left: 20px;
}

.slide_content ul li {
  color: var(--color-grey);
  font-size: 16px;
  margin-bottom: 10px;
}

.box_text_img h3 {
  text-align: center;
  color: var(--color-blue);
  font-family: var(--font-baloo);
  margin-top: 20px;
}

/* Adjust carousel nav positioning if needed */
.carousel-indicators-custom {
  bottom: -50px;
}

.carousel-indicators-custom li {
  background-color: #ddd;
  border-color: #ddd;
}

.carousel-indicators-custom .active {
  background-color: var(--color-blue);
  border-color: var(--color-blue);
}
</style>
