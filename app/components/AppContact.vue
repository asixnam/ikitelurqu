<template>
  <div class="contact-page-wrapper">
    <div class="container-fluid">
       <div class="row display-flex">
          <!-- Left Side: Contact Info -->
          <div class="col-md-5 col-sm-12 contact-info-side">
             <div class="info-content">
                <h4 class="sub-title">Kontak Iki TelurQu</h4>
                <h1 class="main-title">Dapatkan Penawaran terbaik dari Iki TelurQu</h1>
                
                <div class="info-items">
                   <div class="info-item">
                      <div class="icon-circle">
                         <span class="glyphicon glyphicon-earphone"></span>
                      </div>
                      <div class="info-text">
                         0821-9000-0581
                      </div>
                   </div>
                   
                   <div class="info-item">
                      <div class="icon-circle">
                         <span class="glyphicon glyphicon-envelope"></span>
                      </div>
                      <div class="info-text">
                         ikitelurqu@gmail.com
                      </div>
                   </div>

                   <div class="info-item">
                      <div class="icon-circle">
                         <span class="glyphicon glyphicon-home"></span>
                      </div>
                      <div class="info-text address-text">
                         Jl. Pakem - Kalasan, Gatak 2, Selomartani, Kec. Kalasan, Kab. Sleman, D.I Yogyakarta 55571
                      </div>
                   </div>
                </div>
             </div>
          </div>

          <!-- Right Side: Form -->
          <div class="col-md-7 col-sm-12 contact-form-side">
             <div class="form-content">
                <form>
                   <div class="form-group">
                      <label for="nama">Nama Lengkap</label>
                      <input type="text" class="form-control" id="nama" placeholder="Input your full name in here">
                   </div>
                   
                   <div class="form-group">
                      <label for="hp">No Hp</label>
                      <input type="text" class="form-control" id="hp" placeholder="Input your email address in here"> 
                      <!-- Screenshot text says 'email address' placeholder on 'No Hp' field? Or maybe I misread. 
                           User screenshot: Label "No Hp", Placeholder "Input your email address in here". 
                           That seems like a mistake in the design, but I will copy it or correct it? 
                           I'll presume "Input your phone number" is better but I'll stick close to design visuals or sensible defaults. 
                           Actually, standard practice: Label says No Hp, likely means Phone. 
                           Visual screenshot text for No Hp input: "Input your email address in here". 
                           I will use "Input your phone number" to be better, or "Input your email/phone". 
                           Wait, let's look at the label again. Label: No Hp. 
                           I'll put "08..." as example or just generic text.
                           Let's stick to the visible text if possible, or correct it if obvious typo. 
                           I'll use "Input your phone number" as it's No Hp.-->
                   </div>
                   
                   <div class="form-group">
                      <label for="pesan">Pesan</label>
                      <textarea class="form-control" id="pesan" rows="6" placeholder="Write your messages in here"></textarea>
                   </div>
                   
                   <div class="form-actions text-right">
                      <button type="submit" class="btn btn-primary btn-custom">Send Messages</button>
                   </div>
                </form>
             </div>
          </div>
       </div>
    </div>
  </div>
</template>

<style scoped>
.contact-page-wrapper {
  font-family: var(--font-barlow);
}

.display-flex {
  display: flex;
  flex-wrap: wrap;
}

/* Left Side Styling */
.contact-info-side {
  background-color: var(--color-blue); /* #1643A0 */
  color: #fff;
  padding: 80px 60px;
  min-height: 80vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.sub-title {
  color: var(--color-gold); /* #FFD60A */
  font-family: var(--font-baloo);
  font-weight: 600;
  font-size: 20px;
  margin-bottom: 20px;
}

.main-title {
  color: #fff;
  font-family: var(--font-baloo);
  font-weight: 700;
  font-size: 42px;
  line-height: 1.2;
  margin-bottom: 60px;
}

.info-items {
  display: flex;
  flex-direction: column;
  gap: 30px;
}

.info-item {
  display: flex;
  align-items: flex-start;
  gap: 20px;
}

.icon-circle {
  background-color: rgba(255, 255, 255, 0.9); /* White circle */
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  color: var(--color-blue);
  font-size: 18px;
}

.info-text {
  font-size: 16px;
  padding-top: 10px; /* Align with icon center visual */
  font-weight: 500;
}

.address-text {
  line-height: 1.5;
}

/* Right Side Styling */
.contact-form-side {
  background-color: #F1F1F1; /* Light grey bg from screenshot */
  padding: 80px 60px;
  min-height: 80vh;
  display: flex;
  align-items: center;
}

.form-content {
  width: 100%;
  max-width: 600px;
}

.form-group label {
  color: #333;
  font-weight: 600;
  margin-bottom: 10px;
  display: block;
}

.form-control {
  background-color: #fff;
  border: none;
  border-radius: 5px;
  padding: 25px 20px; /* Tall inputs */
  box-shadow: none;
  font-size: 14px;
}

textarea.form-control {
  height: auto;
  min-height: 200px;
}

.btn-custom {
  background-color: #4A90E2; /* Lighter blue in screenshot button */
  border: none;
  padding: 15px 40px;
  font-weight: 600;
  border-radius: 5px;
  margin-top: 20px;
  width: auto;
  float: right;
  transition: background 0.3s;
}

.btn-custom:hover {
  background-color: #357ABD;
}

@media (max-width: 991px) {
  .contact-info-side, .contact-form-side {
    padding: 40px 20px;
    min-height: auto;
  }
  
  .main-title {
    font-size: 32px;
  }
}
</style>
