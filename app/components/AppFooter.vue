<template>
  <footer>
    <div class="footer-area section-bg">
       <div class="container">
          <div class="footer-top section-padding">
             <div class="row">
                <!-- Column 1: Logo -->
                <div class="col-md-3 col-sm-4 mb-50">
                   <div class="footer-logo">
                      <NuxtLink to="/"><img src="/logo.png" alt="Iki TelurQu" class="img-responsive"></NuxtLink>
                   </div>
                   <p style="color: #a0a0a0; margin-top: 20px;">
                     Inovasi olahan telur puyuh dari Jogja untuk Indonesia. Praktis, Lezat, dan Bergizi.
                   </p>
                </div>

                <!-- Column 2: Navigation -->
                <div class="col-md-3 col-sm-4 mb-50">
                   <div class="footer-widget">
                      <h4>Navigation</h4>
                      <ul>
                         <li><NuxtLink to="/">Beranda</NuxtLink></li>
                         <li><NuxtLink to="/profil">Profil</NuxtLink></li>
                         <li><NuxtLink to="/products">Produk</NuxtLink></li>
                         <li><NuxtLink to="/blog">Blog</NuxtLink></li>
                      </ul>
                   </div>
                </div>

                <!-- Column 3: Produk -->
                <div class="col-md-3 col-sm-4 mb-50">
                   <div class="footer-widget">
                      <h4>Produk</h4>
                      <ul>
                         <li><NuxtLink to="/products">Telur Puyuh Bacem</NuxtLink></li>
                         <li><NuxtLink to="/products">Telur Puyuh Kuning</NuxtLink></li>
                         <li><NuxtLink to="/products">Sambal Puyuh</NuxtLink></li>
                         <li><NuxtLink to="/products">Hampers</NuxtLink></li>
                      </ul>
                   </div>
                </div>

                <!-- Column 4: Contact -->
                <div class="col-md-3 col-sm-4 mb-50">
                   <div class="footer-widget">
                      <h4>Contact Person</h4>
                      <ul>
                         <li><a href="https://api.whatsapp.com/send?phone=6282190000716" target="_blank">0821-9000-0716 (Admin)</a></li>
                         <li><a href="mailto:info@ikitelurqu.com">info@ikitelurqu.com</a></li>
                      </ul>
                   </div>
                </div>
             </div>
          </div>
          
          <div class="footer-bottom">
             <div class="row">
                <div class="col-md-12 text-center">
                   <p class="copyright">Copyright &copy; 2026 Iki TelurQu. All Rights Reserved.</p>
                </div>
             </div>
          </div>
       </div>
    </div>
  </footer>
</template>

<style scoped>
.footer-area {
  background: #002535;
  color: #fff;
  font-family: var(--font-poppins);
}

.section-padding {
  padding-top: 80px;
  padding-bottom: 40px;
}

.footer-logo img {
  max-width: 180px;
  padding: 10px;
  border-radius: 5px;
}

.footer-widget h4 {
  color: #fff;
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 30px;
  position: relative;
}

.footer-widget ul li {
  margin-bottom: 15px;
}

.footer-widget ul li a {
  color: #ffffff;
  font-size: 14px;
  font-weight: 400;
  transition: all 0.3s;
}

.footer-widget ul li a:hover {
  color: var(--theme-color);
  padding-left: 5px;
}

.footer-bottom {
  border-top: 1px solid #2d2d31;
  padding: 25px 0;
}

.copyright {
  color: #888;
  font-size: 14px;
  margin: 0;
}

.mb-50 {
  margin-bottom: 50px;
}
</style>
