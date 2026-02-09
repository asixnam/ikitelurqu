<template>
  <header class="site-header" :class="{ 'scrolled': isScrolled }">
    <div class="container header-inner">
      <div class="row align-items-center" style="width: 100%; margin: 0;">
        <!-- Logo -->
        <div class="col-lg-2 col-md-3 col-sm-4 col-xs-6">
          <div class="logo">
             <NuxtLink to="/">
                <img src="/logo.png" alt="Iki TelurQu Logo" class="logo-img" />
             </NuxtLink>
          </div>
        </div>

        <!-- Navigation (Desktop) -->
        <div class="col-lg-8 col-md-7 hidden-sm hidden-xs text-center">
          <nav class="main-menu">
            <ul>
              <li><NuxtLink to="/" exact-active-class="active">Beranda</NuxtLink></li>
              <li><NuxtLink to="/profil" active-class="active">Profil</NuxtLink></li> <!-- Changed from Detail Produk to Profil to match Malond -->
              <li><NuxtLink to="/products" active-class="active">Produk</NuxtLink></li> <!-- Added Products dropdown placeholder if needed -->
              <li><NuxtLink to="/blog" active-class="active">Blog</NuxtLink></li>
              <li><NuxtLink to="/outlet" active-class="active">Outlet</NuxtLink></li>
            </ul>
          </nav>
        </div>

        <!-- Call to Action (Desktop) -->
        <div class="col-lg-2 col-md-2 hidden-sm hidden-xs text-right">
           <a href="https://api.whatsapp.com/send?phone=6281332614978" target="_blank" class="header-btn">
              <i class="glyphicon glyphicon-shopping-cart"></i> Order Online
           </a>
        </div>

        <!-- Mobile Top Right Action -->
        <div class="col-sm-8 col-xs-6 text-right visible-sm visible-xs">
           <a href="https://api.whatsapp.com/send?phone=6281332614978" target="_blank" class="mobile-top-btn">
              <i class="glyphicon glyphicon-shopping-cart"></i>
           </a>
        </div>
      </div>
    </div>

    <!-- Mobile Bottom Navigation -->
    <div class="mobile-bottom-nav">
        <NuxtLink to="/" class="nav-item">
           <i class="glyphicon glyphicon-home"></i>
           <span>Beranda</span>
        </NuxtLink>
        <NuxtLink to="/products" class="nav-item">
           <i class="glyphicon glyphicon-th-large"></i>
           <span>Produk</span>
        </NuxtLink>
        
        <div class="nav-item center-item">
             <a href="https://api.whatsapp.com/send?phone=6281332614978" target="_blank" class="order-fab">
                <i class="glyphicon glyphicon-shopping-cart"></i>
             </a>
        </div>

        <NuxtLink to="/outlet" class="nav-item">
           <i class="glyphicon glyphicon-map-marker"></i>
           <span>Outlet</span>
        </NuxtLink>
        <NuxtLink to="/profil" class="nav-item">
           <i class="glyphicon glyphicon-user"></i>
           <span>Profil</span>
        </NuxtLink>
    </div>
</header>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isMenuOpen = ref(false)
const isScrolled = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.site-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  transition: all 0.3s ease-out;
  padding: 15px 0;
  background: transparent !important; /* Force transparent */
  box-shadow: none; /* No shadow initially */
}

.site-header.scrolled {
  background: #ffffff;
  padding: 10px 0;
}

.header-inner {
  display: flex;
  align-items: center;
}

/* Ensure row content is aligned */
.row.align-items-center {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.logo-img {
  max-width: 80px;
  height: auto;
  display: block; /* Removes bottom space */
}

/* Main Menu */
.main-menu ul {
  display: inline-block;
  margin: 0;
  background: rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  padding: 0 50px;
  border-radius: 100px;
  border: 1px solid rgba(255, 255, 255, 0.4);
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}

.main-menu ul li {
  display: inline-block;
  margin-left: 30px;
  position: relative;
}

.main-menu ul li a {
  color: #000000;
  font-family: var(--font-poppins);
  font-weight: 400;
  font-size: 16px;
  padding: 15px 0;
  display: block;
  text-transform: capitalize;
  line-height: 1; /* Tidy up line height for alignment */
}

.site-header.scrolled .main-menu ul li a {
  color: var(--heading-color);
}

.main-menu ul li a:hover,
.main-menu ul li a.active {
  color: var(--theme-color);
}

/* Header Button */
.header-btn {
  background: var(--theme-color);
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 50px; /* Pill shape looks more professional with icons */
  font-weight: 600;
  font-size: 12px;
  font-family: var(--font-poppins);
  transition: all 0.3s ease;
  display: inline-flex; /* Flex to center icon/text */
  align-items: center;
  justify-content: center;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  text-decoration: none;
  line-height: normal;
  box-shadow: 0 4px 15px rgba(255, 86, 0, 0.3); /* Soft shadow */
}

.header-btn:hover {
  background: #e04b00; /* Darker orange on hover */
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(255, 86, 0, 0.4);
  color: #fff !important;
}

.header-btn i {
  margin-right: 8px;
  font-size: 16px;
  position: relative;
  top: -1px;
}

.site-header.scrolled .header-btn {
  color: var(--heading-color);
  border-color: var(--theme-color);
}

.header-btn:hover {
  background: var(--theme-color);
  color: #fff !important;
}

/* Mobile Top Right Button (Minimalist) */
.mobile-top-btn {
  background: #fff;
  color: var(--theme-color);
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1); /* Subtle shadow */
  border: 1px solid #f0f0f0;
}

.mobile-top-btn i {
  margin: 0;
  font-size: 18px;
}

/* Bottom Navigation (Mobile - Refined) */
.mobile-bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #ffffff;
  box-shadow: 0 -2px 10px rgba(0,0,0,0.1);
  display: none; /* Hidden on desktop by default */
  justify-content: space-around; /* Distribute space evenly */
  align-items: center;
  padding: 0 10px;
  height: 65px; /* Standard visible height */
  z-index: 1002;
  border-top: 1px solid #f0f0f0;
}

.nav-item {
  display: flex;
  flex-direction: column; /* Stack icon and text */
  align-items: center;
  justify-content: center;
  text-decoration: none;
  color: #fbaf02; /* Gold color */
  font-family: var(--font-poppins);
  transition: all 0.3s;
  flex: 1;
  height: 60%;
  background: none;
  border: none;
  margin: 0;
  padding: 5px 0 0;
  position: relative;
}

.nav-item span {
  display: block; /* Show text */
  font-size: 10px;
  margin-top: 2px;
  font-weight: 500;
}

.nav-item i {
  font-size: 16px;
  color: #fbaf02; /* Gold color */
  transition: all 0.3s;
  margin-bottom: 2px;
}

.nav-item:hover,
.nav-item.router-link-active {
  color: var(--theme-color);
  text-decoration: none;
}

.nav-item:hover i,
.nav-item.router-link-active i {
  color: var(--theme-color);
  transform: translateY(-2px);
}

/* Center Floating Action Button (FAB) */
.center-item {
  position: relative;
  /* top: -20px;  Pull it up */
  overflow: visible;
  flex: 0 0 70px; /* Fixed width for the center area */
}

.order-fab {
  width: 60px;
  height: 60px;
  background: #fbaf02; /* Gold color */
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 24px; /* Icon size */
  box-shadow: 0 4px 10px rgba(251, 175, 2, 0.4);
  position: absolute;
  bottom: 15px; /* Float above bar */
  left: 50%;
  transform: translateX(-50%);
  border: 4px solid #fff; /* White ring to separate from bar content visually if needed, or just style */
  z-index: 1003;
  transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.order-fab:hover {
  transform: translateX(-50%) scale(1.1);
  box-shadow: 0 6px 15px rgba(251, 175, 2, 0.5);
  color: #fff;
}

.order-fab i {
  color: #fff;
  font-size: 24px;
}


/* Mobile Menu Overlay */
.mobile-menu-overlay {
  position: fixed;
  bottom: 0; /* Align to bottom, behind nav */
  left: 0;
  width: 100%;
  height: auto;
  min-height: 50vh;
  background: #fff;
  z-index: 1001;
  box-shadow: 0 -5px 20px rgba(0,0,0,0.15);
  transition: transform 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  transform: translateY(100%); /* Slide down to hide */
  top: auto; /* Reset top */
  padding: 30px 20px 90px; /* Bottom padding for nav bar */
  border-radius: 20px 20px 0 0;
}

.mobile-menu-overlay.open {
  transform: translateY(0); /* Slide up to show */
}

.menu-title {
  font-family: var(--font-poppins);
  font-weight: 700;
  color: var(--heading-color);
  margin-bottom: 20px;
  text-align: center;
}


.mobile-menu-content {
  display: flex;
  flex-direction: column;
}

.menu-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
  gap: 15px;
}

.menu-grid-item {
  width: calc(33.333% - 10px); /* 3 items per row */
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  background: #f9f9f9;
  border-radius: 15px;
  padding: 15px 5px;
  margin-bottom: 10px;
  transition: all 0.3s;
}

.menu-grid-item i {
  font-size: 24px;
  color: var(--theme-color);
  margin-bottom: 8px;
}

.menu-grid-item span {
  font-family: var(--font-poppins);
  color: var(--heading-color);
  font-size: 12px;
  font-weight: 500;
  text-align: center;
}

.menu-grid-item:hover {
  background: #fff;
  box-shadow: 0 5px 15px rgba(0,0,0,0.05);
  transform: translateY(-2px);
}

/* Adjustments for transparency issue see below */

@media (max-width: 991px) {
  .site-header {
      background: #fff !important; /* Force white background for readability */
      position: fixed; /* Keep it fixed as requested */
      top: 0;
      width: 100%;
      z-index: 1000;
      box-shadow: 0 0 5px rgba(0,0,0,0.1);
  }
  .site-header.scrolled {
      padding: 15px 0;
  }
  
  :global(body) {
      padding-bottom: 70px; /* Prevent content from being hidden behind bottom nav */
  }

  .mobile-bottom-nav {
      display: flex; /* Show only on mobile/tablet */
  }
}
</style>

