<template>
  <div class="bg-color" id="tjanster">
    <!-- <div class="py-5 container text-white wow fadeIn" style="animation-delay: 1000ms;">
      <h1 class="theme-color">Våra tjänster</h1>
      <hr class="my-4 theme-bg">
      <p class="mb-0">
        Vi projekterar och konstruerar rörsystem för energi-och processindustri. Detta innefattar:
      </p>
      <ul class="text-white mt-3 ml-0">
        <li class="visited">Mekanisk konstruktion av rör och tryckkärl</li>
        <li class="visited">Hållfasthetsberäkning och spänningsanalys av rörsystem</li>
        <li class="visited">Projektledning</li>
        <li class="visited">Projektering och visualisering i 3D Cad</li>
        <li class="visited">Vi administrerar CE-processen och tar fram erforderlig dokumentation och beräkningar.</li>
      </ul>
    </div> -->
    <div class="container pb-5 py-5 pb-sm-0 wow fadeIn" style="animation-delay: 1000ms;">
      <div class="row text-white">
        <div class="col-md-8">
          <h1 class="theme-color">Våra tjänster</h1>
          <hr class="my-4 theme-bg">
          <p class="mb-0">
            Vi projekterar och konstruerar rörsystem för energi-och processindustri. Detta innefattar:
          </p>
          <ul class="text-white mt-3 ml-0">
            <li class="visited">Mekanisk konstruktion av rör och tryckkärl</li>
            <li class="visited">Hållfasthetsberäkning och spänningsanalys av rörsystem</li>
            <li class="visited">Projektledning</li>
            <li class="visited">Projektering och visualisering i 3D Cad</li>
            <li class="visited">Vi administrerar CE-processen och tar fram erforderlig dokumentation och beräkningar.</li>
          </ul>
        </div>
        <div class="col-md-4 justify-content-center d-flex my-auto">
          <img src="@/assets/3D.gif" class="rounded" alt="...">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.bg-color {
  background: rgb(31, 31, 31);
}

ul {
  list-style: none;
  margin: 50px;
  padding: 20;
}

.visited {
  padding-bottom: 5px !important;
}

li {
  /* overflow: hidden; */
  position: relative;
  padding: 0 0 10px 35px;
}

li::before {
  /* content: '';
  position: absolute;
  left: 5px;
  top: 8px;
  width: 20px;
  height: 25px;
  border: 2px solid lightgray;
  border-width: 2px 0 0 2px; */
}

li:last-child::before {
  border-width: 2px 0 0 0;
}

li::after {
  content: '';
  position: absolute;
  left: 0;
  top: 3px;
  width: 8px;
  height: 8px;
  background: #fff;
  border: 2px solid lightgray;
  border-radius: 50%;
}

li.current::before {
  border-top-color: var(--theme-color);
}
li.current::after {
  border-color: var(--theme-color);
  background: var(--theme-color);
}
li.visited { padding-left: 18px;}
li.visited::before,
li.visited::after {
  border-color: var(--theme-color);
  margin-top: 4.5px;
}



</style>