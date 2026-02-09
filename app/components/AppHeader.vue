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
    <div class="mobile-bottom-nav visible-xs visible-sm">
        <NuxtLink to="/" class="nav-item">
           <i class="glyphicon glyphicon-home"></i>
           <span>Beranda</span>
        </NuxtLink>
        <NuxtLink to="/products" class="nav-item">
           <i class="glyphicon glyphicon-th-large"></i>
           <span>Produk</span>
        </NuxtLink>
        <div class="nav-item">
             <a href="https://api.whatsapp.com/send?phone=6281332614978" target="_blank" class="order-btn">
                <i class="glyphicon glyphicon-shopping-bag"></i> <!-- Changed to bag to match image -->
             </a>
        </div>
        <NuxtLink to="/outlet" class="nav-item">
           <i class="glyphicon glyphicon-map-marker"></i>
           <span>Outlet</span>
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

/* Bottom Navigation (Mobile - Image Match) */
.mobile-bottom-nav {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background: #ffffff;
  box-shadow: 0 -5px 20px rgba(0,0,0,0.1);
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0; /* Remove padding for dividers to touch edges */
  height: 70px; /* Fixed height */
  z-index: 1002;
  border-radius: 25px 25px 0 0; /* Rounded top like image */
}

.nav-item {
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  color: #fbaf02; /* Match the yellow/orange icon color from image */
  font-family: var(--font-poppins);
  transition: all 0.3s;
  flex: 1;
  height: 100%;
  background: none;
  border: none;
  border-right: 1px solid #f0f0f0; /* Vertical divider */
  margin: 0;
  padding: 0;
}

.nav-item:last-child {
  border-right: none;
}

.nav-item span {
  display: none; /* Hide text as per image */
}

.nav-item i {
  font-size: 24px;
  color: #fbaf02; /* Explicit yellow/orange */
  transition: all 0.3s;
}

.nav-item:hover i,
.nav-item.router-link-active i {
  color: var(--theme-color); /* Darker orange on active/hover */
  transform: scale(1.1);
}

/* Center Item Adjustment */
.center-item {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}

.order-btn {
  /* Resetting order btn to look like a normal icon in this layout if desired, 
     OR keeping it distinct. The image shows standard icons. 
     I will make it blend in as an icon for consistency with the "row of icons" look. 
  */
  width: auto;
  height: auto;
  background: none;
  box-shadow: none;
  border: none;
  color: #fbaf02;
}

.order-btn i {
  font-size: 24px;
  color: #fbaf02;
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
}
</style>

