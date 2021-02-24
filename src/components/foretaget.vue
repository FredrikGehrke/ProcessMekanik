<template>
    <div class="py-5 z-depth-1 bg-color">
        <section class="white-text container animated fadeIn ">
            <div class="row pr-lg-5">
                <div class="col-md-7 mb-4">

                  <div class="col-md-11 animated">
                      <!-- Google Maps -->
                      <div id="map-within-card-2" class="map-container rounded-left rounded-right z-depth-5 wow fadeIn" style="height: 320px">
                          <iframe src="https://maps.google.com/maps?q=Legeringsgatan6&t=&z=13&ie=UTF8&iwloc=&output=embed" frameborder="0"
                          style="border:0" allowfullscreen></iframe>
                      </div>
                      <!-- Google Maps -->
                  </div>

                </div>
                <div class="col-md-5 d-flex align-items-center">
                    <div>
                    
                    <h1 class="font-weight-bold mb-2 theme-color wow fadeIn" style="animation-delay: 400ms;">Om företaget</h1>
                    <div class="wow fadeIn" style="animation-delay: 500ms;">
                      <p class="mb-4">Vi startade år 2000 och är två ingenjörer.</p>

                      <p>Vi finns i Teknikbyn i Västerås. Våra kunder är energiproducenter och anläggningsleverantörer, främst i Mälardalen.</p>
                      <p class="font-weight-bold">Vi tar gärna ansvar för upphandling och projektledning i kundens projekt.</p>

                      <router-link to="/kontakta-oss" class="btn theme-bg animated fadeIn ml-0" style="animation-delay: 900ms;">KONTAKT</router-link>
                    </div>


                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.bg-color {
  background: rgb(37, 37, 37);
}

.map-container {
  overflow: hidden;
  position: relative;
  height: 0;
}

.map-container iframe {
  left: 0;
  top: 0;
  height: 100%;
  width: 100%;
  position: absolute;
}

.btn {
  font-size: 16px;
}

</style>