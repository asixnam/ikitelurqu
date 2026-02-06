<template>
  <div class="page-home">
    <HomeHero />
    <HomeLegalitas />
    <!-- Profil section is commented out in source but I will include it if requested "persis" as it was in CSS source, 
         actually in source it was commented out: <!-- <div class="profil">... -->
    <!-- However, the user said "persis seperti di website ini". On the live site, is it visible?
         The prompt implies "persis seperti di website ini" (exactly like this website).
         If the HTML source I fetched had it commented out, likely it's NOT on the live site.
         I will keep it available but maybe commented out or included if the design requires it.
         Wait, let's look at `site_source.html` again.
         Line 159: `<!-- <div class="profil">`
         So it is NOT visible on the live site if the live site matches the source I got.
         But the user might want the "design" including parts that are "there".
         Let's assume we render what is VISIBLE.
         Visible order: Header -> Legalitas -> Latarbelakang -> Kandungan -> Profil (Wait, Line 327 `div class="profil"` is NOT commented out! 
         Ah, there were TWO profil blocks in source??
         Line 159 is commented out.
         Line 327 is NOT commented out.
         So Profil IS visible later down the page.
    -->
    
    <HomeFeatures /> <!-- Latarbelakang -->
    
    <HomeKandungan />
    
    <HomeProfil /> <!-- The visible one around line 327 -->
    
    <HomeProcess /> <!-- Produksi -->
    
    <HomeProducts /> <!-- Produk -->
    
    <HomeContact /> <!-- Kontak Market -->
    
    <!-- Footer is in layout -->
  </div>
</template>

<script setup>
// Components are auto-imported by Nuxt
</script>
