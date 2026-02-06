<template>
  <header class="site-header navbar-custom">
    <div class="container header-inner">
      <!-- Brand / Logo -->
      <div class="header-left">
         <NuxtLink to="/" class="brand-link">
            <img src="/logo.png" alt="Iki TelurQu Logo" class="logo-img" />
         </NuxtLink>
         <!-- Decorative line -->
         <div class="decorative-line"></div>
      </div>

      <!-- Navigation (Desktop) -->
      <nav class="site-nav hidden-xs hidden-sm">
        <ul class="nav-links">
          <li><NuxtLink to="/" class="nav-item" active-class="active">Beranda</NuxtLink></li>
          <li><NuxtLink to="/profil" class="nav-item" active-class="active">Detail Produk</NuxtLink></li>
          <li><NuxtLink to="/outlet" class="nav-item" active-class="active">Outlet</NuxtLink></li>
        </ul>
      </nav>

      <!-- Market Links (Desktop) -->
      <div class="menu_market hidden-xs hidden-sm">
          <ul>
            <li><a href="#" target="_blank"><img src="https://ikitelurqu.com/asset_front/img/ic_shopee.png" alt="Shopee"></a></li>
            <li><a href="#" target="_blank"><img src="https://ikitelurqu.com/asset_front/img/ic_tokped.png" alt="Tokopedia"></a></li>
            <li><a href="#" target="_blank"><img src="https://ikitelurqu.com/asset_front/img/ic_tiktok.png" alt="TikTok"></a></li>
          </ul>
      </div>

      <!-- Mobile Menu Toggle -->
      <button class="mobile-toggle visible-xs visible-sm" aria-label="Menu" @click="toggleMenu">
        <span class="bar" :class="{ 'open': isMenuOpen }"></span>
        <span class="bar" :class="{ 'open': isMenuOpen }"></span>
        <span class="bar" :class="{ 'open': isMenuOpen }"></span>
      </button>

      <!-- Mobile Navigation Overlay -->
      <div class="mobile-nav-overlay" :class="{ 'open': isMenuOpen }">
         <div class="mobile-nav-content">
            <NuxtLink to="/" class="mobile-link" @click="isMenuOpen = false">Beranda</NuxtLink>
            <NuxtLink to="/profil" class="mobile-link" @click="isMenuOpen = false">Detail Produk</NuxtLink>
            <NuxtLink to="/outlet" class="mobile-link" @click="isMenuOpen = false">Outlet</NuxtLink>
         </div>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const isMenuOpen = ref(false)
const toggleMenu = () => isMenuOpen.value = !isMenuOpen.value
</script>

<style scoped>
/* Strict Layout Reset */
.site-header {
  height: 90px;
  background-color: rgba(255, 255, 255, 0.98);
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 1000;
  box-shadow: 0 4px 20px rgba(0,0,0,0.05);
  border-bottom: 1px solid #f0f0f0;
}

.header-inner {
  height: 100%;
  display: flex !important; /* Override bootstrap floats */
  justify-content: space-between;
  align-items: center;
  position: relative;
}

/* Header Left (Logo area) */
.header-left {
  position: relative;
  height: 100%;
  display: flex;
  align-items: center;
  /* Ensure it doesn't collapse */
  min-width: 150px; 
  gap: 15px; /* Space between logo and line */
}

.brand-link {
  display: block;
  z-index: 1002; /* Above mobile menu */
}

.logo-img {
  height: 60px; /* Fixed height for consistency */
  width: auto;
  display: block;
}

.decorative-line {
  position: relative;
  bottom: auto;
  left: auto;
  width: 500px; /* Horizontal length */
  height: 2px; /* Thickness */
  background-color: var(--color-blue);
  border-radius: 2px; /* Rounded ends */
  margin-left: 5px; /* Slight adjustment if gap is 15px */
}

/* Desktop Nav */
.nav-links {
  display: flex;
  gap: 40px;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-item {
  font-family: var(--font-baloo);
  font-weight: 700;
  font-size: 18px;
  color: var(--color-blue);
  text-decoration: none;
  padding: 5px 0;
  position: relative;
  transition: color 0.3s;
}

.nav-item:after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: var(--color-red);
  transition: width 0.3s;
}

.nav-item:hover:after, .nav-item.active:after {
  width: 100%;
}

.nav-item:hover, .nav-item.active {
  color: var(--color-red);
}

/* Market Links */
.menu_market ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  gap: 15px;
}

.menu_market ul li a img {
  height: 35px;
  width: auto;
  transition: transform 0.2s;
}

.menu_market ul li a img:hover {
  transform: scale(1.1);
}

/* Mobile Toggle */
.mobile-toggle {
  background: none;
  border: none;
  padding: 10px;
  cursor: pointer;
  z-index: 1002;
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.bar {
  width: 30px;
  height: 3px;
  background-color: var(--color-blue);
  transition: all 0.3s;
  border-radius: 3px;
}

.bar.open:nth-child(1) { transform: rotate(45deg) translate(5px, 6px); }
.bar.open:nth-child(2) { opacity: 0; }
.bar.open:nth-child(3) { transform: rotate(-45deg) translate(5px, -6px); }

/* Mobile Nav Overlay */
.mobile-nav-overlay {
  position: fixed;
  top: 90px;
  left: 0;
  width: 100%;
  height: calc(100vh - 90px);
  background-color: white;
  transform: translateX(100%);
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
}

.mobile-nav-overlay.open {
  transform: translateX(0);
}

.mobile-nav-content {
  display: flex;
  flex-direction: column;
  gap: 30px;
  text-align: center;
}

.mobile-link {
  font-family: var(--font-baloo);
  font-size: 24px;
  font-weight: 700;
  color: var(--color-blue);
  text-decoration: none;
}

.mobile-link.router-link-active {
  color: var(--color-red);
}

@media (max-width: 991px) { /* Tablet adjustments */
  .site-header { height: 70px; }
  .logo-img { height: 45px; }
  .mobile-nav-overlay { top: 70px; height: calc(100vh - 70px); }
}
</style>
