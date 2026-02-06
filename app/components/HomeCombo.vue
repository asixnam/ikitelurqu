<template>
  <div class="kombo_makanan">
     <div class="container">
        <div class="title_kombo_makanan">
           <h3>Kombo makanan terbaik</h3>
           <h2>Apapun makannya, <br> Iki TelurQu pelengkapnya!</h2>
        </div>

        <div class="img_kombinasi_makan_ikitelurqu">
           <img src="https://ikitelurqu.com/asset_front/img/kombinasi_makanan_ikitelurqu.png" class="img-responsive" alt="Image">
        </div>
     </div>
  </div>
</template>

<style scoped>
.kombo_makanan {
  padding-top: 100px;
  padding-bottom: 100px;
  background-color: var(--color-bg-light);
}

.title_kombo_makanan {
  padding-bottom: 60px;
  text-align: center;
}

.title_kombo_makanan h3 { margin: 0; color: var(--color-grey); }
.title_kombo_makanan h2 { 
  margin: 0; 
  color: var(--color-blue); 
  font-family: var(--font-baloo); 
  font-weight: 700; 
  font-size: 40px;
}

.img_kombinasi_makan_ikitelurqu {
  display: flex;
  justify-content: center;
}
</style>
