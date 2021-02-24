<template>
  <div>
    <navbar />
    <banner />
    <tjanster />
    <foretaget />
    <kontakt />
    <referenser />
    <myFooter />
  </div>
</template>

<script>
import navbar from './components/navbar'
import banner from './components/banner'
import foretaget from './components/foretaget'
import myFooter from './components/footer'
import referenser from './components/referenser'
import tjanster from './components/tjanster'
import kontakt from './components/kontakt'

export default {
  name: 'App',
  components: {
    navbar,
    banner,
    foretaget,
    myFooter,
    referenser,
    tjanster,
    kontakt
  }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: 0;
  letter-spacing: 1.5px;
  font-family: 'Poppins', sans-serif;
}

html {
  scroll-behavior: smooth;
}

:root {
  --theme-color: #2979ff;
}

.theme-bg {
  background-color: var(--theme-color)
}

.theme-color {
  color: var(--theme-color)
}

.bg-color {
  background-color: rgba(230, 228, 228, 0.192);
}

.title-color {
  color: #2979ff;
}

.btn:hover {
  box-shadow: 0px 0px 20px 2px #4b8af7;  
  color: white;
}

h1, h2, h3, h4 , h5 {
  font-family: 'Poppins', sans-serif;
  font-weight: bold;
}


.dark-bg {
  background: linear-gradient(to bottom, rgb(32, 32, 32), rgb(19, 19, 19));
  box-shadow: 0px 5px 20px 10px rgba(0, 0, 0, 0.219);  
}

.lighter-bg {
  background-color: rgba(230, 228, 228, 0.192);
}

::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: #1B242F; 
  box-shadow: inset 0 0 6px rgb(7, 6, 6); 
}

::-webkit-scrollbar-thumb {
  background: var(--theme-color); 
  -webkit-border-radius: 50px;
  border-radius: 50px;
}

::-webkit-scrollbar-thumb:hover{
  background: #669af5; 
}

</style>
