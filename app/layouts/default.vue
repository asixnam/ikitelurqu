<template>
  <div class="layout-default">
    <AppHeader />
    
    <main class="site-content">
      <slot />
    </main>
    
    <AppFooter />
  </div>
</template>

<style scoped>
.layout-default {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.site-content {
  flex: 1;
  /* Since header is absolute, we might need padding-top on content pages, 
     but HomeHero.vue handles it with .header_page { padding-top: 100px; }.
     Other pages might need manual padding.
  */
}
</style>
