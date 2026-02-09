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
  font-family: var(--font-poppins);
}

.display-flex {
  display: flex;
  flex-wrap: wrap;
}

/* Left Side Styling */
.contact-info-side {
  background-color: var(--heading-color); /* Dark Black/Blue #16161a */
  color: #fff;
  padding: 80px 60px;
  min-height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.sub-title {
  color: var(--theme-color); /* Orange */
  font-family: var(--font-josefin);
  font-weight: 600;
  font-size: 18px;
  margin-bottom: 20px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.main-title {
  color: #fff;
  font-family: var(--font-poppins);
  font-weight: 700;
  font-size: 36px;
  line-height: 1.3;
  margin-bottom: 50px;
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
  background-color: rgba(255, 255, 255, 0.1); /* Transparent/Glassy */
  width: 50px;
  height: 50px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  color: var(--theme-color);
  font-size: 20px;
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.info-text {
  font-size: 16px;
  padding-top: 12px;
  font-weight: 400;
  color: #ddd;
}

.address-text {
  line-height: 1.6;
}

/* Right Side Styling */
.contact-form-side {
  background-color: #f7f7fd; /* Light grey/blueish bg */
  padding: 80px 60px;
  min-height: 600px;
  display: flex;
  align-items: center;
}

.form-content {
  width: 100%;
  max-width: 600px;
}

.form-group label {
  color: var(--heading-color);
  font-weight: 600;
  margin-bottom: 10px;
  display: block;
  font-size: 14px;
}

.form-control {
  background-color: #fff;
  border: 1px solid #eee;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.02);
  font-size: 14px;
  transition: all 0.3s;
  font-family: var(--font-poppins);
}

.form-control:focus {
  border-color: var(--theme-color);
  box-shadow: 0 5px 20px rgba(0,0,0,0.05);
}

textarea.form-control {
  height: auto;
  min-height: 150px;
}

.btn-custom {
  background-color: var(--theme-color);
  color: #fff;
  border: none;
  padding: 15px 40px;
  font-weight: 600;
  border-radius: 50px;
  margin-top: 20px;
  width: auto;
  transition: all 0.3s;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  font-size: 14px;
  box-shadow: 0 10px 30px rgba(255, 86, 0, 0.3);
}

.btn-custom:hover {
  background-color: #e04b00;
  transform: translateY(-3px);
  box-shadow: 0 15px 35px rgba(255, 86, 0, 0.4);
}

@media (max-width: 991px) {
  .contact-info-side, .contact-form-side {
    padding: 50px 20px;
    min-height: auto;
  }
  
  .main-title {
    font-size: 28px;
  }
}
</style>
