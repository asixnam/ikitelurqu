<template>
  <div class="contac_footer">
    <div class="container">
       <!-- Footer Bottom Section -->
       <div class="row">
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="link_menu_footer">
                <ul>
                   <li><NuxtLink to="/">Beranda</NuxtLink></li>
                   <li><NuxtLink to="/profil">Detail Produk</NuxtLink></li>
                   <li><NuxtLink to="/outlet">Outlet</NuxtLink></li>
                   <li><NuxtLink to="/blog">Blog</NuxtLink></li>
                </ul>
             </div>
             <p class="copyright visible-xs text-center">&copy; 2026 Iki TelurQu</p>
          </div>
          <div class="col-xs-12 col-sm-12 col-md-6 col-lg-6">
             <div class="menu_link">
                <!-- Social Media -->
                <div class="menu_sosial_media">
                   <ul>
                      <li><a href="#" target="_blank"><img src="https://ikitelurqu.com/asset_front/img/Facebook.png" alt="Facebook"></a></li>
                      <li><a href="#" target="_blank"><img src="https://ikitelurqu.com/asset_front/img/TikTok.png" alt="TikTok"></a></li>
                      <li><a href="#" target="_blank"><img src="https://ikitelurqu.com/asset_front/img/Instagram.png" alt="Instagram"></a></li>
                   </ul>
                </div>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.contac_footer {
  padding-top: 50px;
  padding-bottom: 50px;
  background-color: #FFC300;
  color: white;
}

.link_menu_footer {
  padding-top: 15px;
}

.link_menu_footer ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.link_menu_footer ul li {
  display: inline-block;
  margin-right: 25px;
}

.link_menu_footer ul li a {
  color: #FFF;
  font-family: var(--font-baloo);
  font-size: 18px; 
  font-weight: 500;
  text-decoration: none;
  opacity: 0.8;
  transition: opacity 0.2s;
}

.link_menu_footer ul li a:hover {
  opacity: 1;
  color: var(--color-gold);
}

.menu_link {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 15px;
}

.menu_market ul, .menu_sosial_media ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  gap: 15px;
}

.menu_market ul li a img, .menu_sosial_media ul li a img {
  height: 35px;
  width: auto;
  transition: transform 0.2s;
}

.menu_market ul li a img:hover, .menu_sosial_media ul li a img:hover {
  transform: scale(1.1);
}

.copyright {
  margin-top: 20px;
  color: rgba(255,255,255,0.5);
}

@media (max-width: 992px) {
  .menu_link {
    align-items: center; /* Center on mobile */
    margin-top: 30px;
  }
  
  .link_menu_footer {
    text-align: center;
  }
  
  .link_menu_footer ul li {
    display: block; /* Stack links on mobile? Or keep inline? Inline is better usually, let's keep inline but centered */
    margin: 0 10px 10px 10px;
  }
}
</style>
