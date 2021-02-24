<template>
    <div class="bg-img">
        <div class="my-overlay">
            <section class="text-center">
                <div class="col-md-12 p-0">
                    <div class="card">
                        <div class="text-white text-center align-items-center px-4 px-md-5 my-margin-top">
                            <div>
                              <h1 class="py-1 font-weight-bold animated fadeIn" style="animation-delay: 700ms;">
                                <strong class="welcome">Välkommen till ProcessMekanik</strong>
                              </h1>
                              <p id="slogan" class="animated fadeIn" style="animation-delay: 800ms;">
                                Vi är konsulten som projekterar rör- och processanläggningar för <br> energiproducenter och industri.
                              </p>
                              <a href="#tjanster" class="btn wow fadeInUp" style="animation-delay: 900ms;">Tjänster</a>
                              <a href="#kontakt" class="btn wow fadeInUp" style="animation-delay: 900ms;">Kontakt</a>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>


<style scoped>

.btn {
  background: linear-gradient(to right, #2979ff, #262c70);
  border-radius: 10px;
  font-weight: bold;
  font-size: 16px;
  letter-spacing: 1.5px;
  margin: 8px;
  color: white;
  padding: 12px 30px
}

.welcome {
  font-size: 35px;
}

#slogan {
  font-size: 24px !important;
}

.bg-img {
  background-image: url(../assets/vent.jpg);
  background-size: cover;
}

@media (min-width: 768px) {  
  .SBUH {
    font-size: 50px;
  }
  #slogan {
    font-size: 28px;
  }
}

.my-margin-top {
  margin-top: 13%;
}

.card {
  background-color: rgba(27, 27, 27, 0.534);
  padding-bottom: 15%;
}

.my-overlay {
  background: rgba(0, 0, 0, 0.781);
}

</style>
