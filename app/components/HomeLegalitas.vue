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
/* Removing negative margin that pulled it up, allowing it to sit naturally or be pulled by next section */
.grid_legalitas {
  position: relative;
  z-index: 10; /* Ensure it sits on top */
  margin-top: 0; 
  margin-bottom: 10px;
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

.box_grid_legal img {
  max-height: 70%;
  max-width: 80%;
  object-fit: contain;
}

/* Colors - Transparent as requested */
.blod1 { background-color: rgba(0, 53, 102, 0.85); } /* Deep Blue Transparent */
.blod2 { background-color: rgba(2, 145, 63, 0.85); }  /* Green Transparent */
.blod3 { background-color: rgba(130, 40, 135, 0.85); } /* Purple Transparent */

@media (max-width: 768px) {
  .grid_legalitas {
    margin-top: 0;
    margin-bottom: 0px;
  }
}
</style>
