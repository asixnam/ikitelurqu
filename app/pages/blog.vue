<template>
  <div class="page-blog">
    <div class="container blog-container">
      <div class="blog-empty-state">
         <div class="icon-wrap">
            <span class="glyphicon glyphicon-pencil"></span>
         </div>
         <h1 class="main-title">Blog Iki TelurQu</h1>
         <p class="sub-text">Halaman ini sedang dalam proses pengembangan. Nantikan artikel menarik seputar kesehatan dan resep masakan!</p>
         <NuxtLink to="/" class="btn-theme">Kembali ke Beranda</NuxtLink>
      </div>
    </div>
  </div>
</template>

<style scoped>
.page-blog {
  min-height: 80vh;
  background-color: #f7f7fd;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 100px 0;
}

.blog-empty-state {
  text-align: center;
  background: #fff;
  padding: 60px 30px;
  border-radius: 20px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.05);
  max-width: 600px;
  margin: 0 auto;
}

.icon-wrap {
  width: 80px;
  height: 80px;
  background: #fff3e6; /* Light Orange */
  color: var(--theme-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 30px;
  margin: 0 auto 30px;
}

.main-title {
  font-family: var(--font-poppins);
  font-weight: 700;
  color: var(--heading-color);
  margin-bottom: 20px;
  font-size: 32px;
}

.sub-text {
  font-family: var(--font-poppins);
  color: #666;
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 40px;
}

.btn-theme {
  background-color: var(--theme-color);
  color: #fff;
  padding: 15px 35px;
  border-radius: 50px;
  text-decoration: none;
  font-family: var(--font-poppins);
  font-weight: 600;
  display: inline-block;
  transition: all 0.3s;
  box-shadow: 0 5px 15px rgba(255, 86, 0, 0.3);
}

.btn-theme:hover {
  background-color: #e04b00;
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(255, 86, 0, 0.4);
  color: #fff;
}
</style>
