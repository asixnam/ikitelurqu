<template>
  <div class="grid_legalitas">
    <div class="container">
       <div class="row">
          <div class="col-xs-4 col-sm-4 col-md-4 mb-20">
             <div class="box_grid_legal blod1">
                <!-- User changed to local paths, keeping them. Ensure they are centered and sized right. -->
                <img src="/logo_nkv.png" class="img-responsive" alt="NKV">
             </div>
          </div>
          <div class="col-xs-4 col-sm-4 col-md-4 mb-20">
             <div class="box_grid_legal blod2">
                <img src="/logo_bpom.png" class="img-responsive" alt="BPOM">
             </div>
          </div>
          <div class="col-xs-4 col-sm-4 col-md-4 mb-20">
             <div class="box_grid_legal blod3">
                <img src="/logo_halal.png" class="img-responsive" alt="Halal">
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.grid_legalitas {
  position: relative;
  /* The original likely had it overlapping the hero or the next section. 
     User said "perbaiki". 
     Let's use a cleaner negative margin approach or transform to float it up.
     If HomeHero has huge padding top, maybe this sits ON TOP of the hero bottom?
     Or between Hero and Next section?
     Let's try a standard elegant card grid.
  */
  margin-top: -100px; /* Pull it up to overlap the previous section (Hero) slightly if that's the design */
  z-index: 10;
  margin-bottom: 50px;
}

.box_grid_legal {
  width: 100%;
  height: 140px; 
  border-radius: 15px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  transition: transform 0.3s;
  padding: 20px;
}

.box_grid_legal:hover {
  transform: translateY(-5px);
}

.box_grid_legal img {
  max-height: 80%;
  max-width: 80%;
  object-fit: contain;
}

/* Colors with slightly better opacity handling if needed, or keeping original solid with alpha */
.blod1 { background-color: rgba(0, 53, 102, 0.9); } /* #003566 */
.blod2 { background-color: rgba(2, 145, 63, 0.9); }  /* Green */
.blod3 { background-color: rgba(130, 40, 135, 0.9); } /* Purple */

.mb-20 {
  margin-bottom: 20px;
}

@media (max-width: 768px) {
  .grid_legalitas {
    margin-top: 20px; /* No negative margin on mobile */
    margin-bottom: 20px;
  }
}
</style>
