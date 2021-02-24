<template>
  <div class="container-fluid pb-5 dark-bg" id="kontakt">
    <div class="container">
      <div class="text-center text-white">
        <p class="pt-5 wow heartBeat h1 font-weight-bold" data-wow-duration="2s">Kontakt</p>
        <hr class="mb-4" />
        <h6>Skicka gärna ett meddelande!</h6>
      </div>
      <div class="d-block d-md-flex mt-5 mt-sm-0">
        <div class="col-md-6">
          <!-- <i class="fas fa-map-marker-alt fa-2x mt-3 theme-color mb-2"></i>
          <p class="font-weight-bold mb-0 text-white">
            Västerås, Sverige
          </p>
          <a href="tel:070-7425886"><i class="fas fa-phone-square-alt fa-2x theme-color mt-5 mb-2"></i></a>
          <ul class="list-unstyled text-white font-weight-bold">
            <li>
                <a href="tel:070-7425886">070-7425886</a>
            </li>
          </ul>
          <a href="mailto:thomas.claesson@processmekanik.se"><i class="fas fa-envelope fa-2x theme-color mt-5"></i></a>
          <ul class="list-unstyled font-weight-bold">
            <li>
                <a href="mailto:leif@sbuh.se">thomas.claesson@processmekanik.se</a>
            </li>
          </ul> -->

          <div class="d-flex h-100">
            <div class="row justify-content-center align-self-center text-center m-auto">
                <div class="w-100 d-flex justify-content-center align-items-center custom-bg z-depth-3">
                    <img src="@/assets/thomas.jpg" class="img-fluid rounded-circle z-depth-3"/>
                </div>
                <div class="mt-3">
                  <h5 class="font-weight-bold mt-4 mb-2 white-text">Thomas Claesson</h5>
                  <p class="text-uppercase font-weight-bold theme-color mb-2">Världserövrare</p>
                  <div class="d-none d-xl-block">
                    <div>
                      <i class="fas fa-envelope fa-lg theme-color">
                          <a class="white-text my-text-size" href="mailto:thomas.claesson@processmekanik.se">thomas.claesson@processmekanik.se</a> 
                      </i>
                    </div>
                    <div>
                      <i class="fas fa-phone fa-lg theme-color pt-2">
                          <a class="white-text my-text-size" href="tel:0707425886">073-534 33 93</a>  
                      </i>                                        
                    </div>
                  </div>
                  <div class="d-xl-none">
                    <i class="fas fa-phone fa-lg theme-color pt-2"></i>
                    <i class="fas fa-envelope fa-lg theme-color ml-2"></i>   
                  </div>

                </div>                 
            </div>
          </div>

        </div>
        
        <form @submit.prevent="sendEmail" class="col-md-6 mt-5 mx-auto text-white" >
          <div class="form-group">
            <label for="exampleFormControlInput1">Namn<span class="theme-color">*</span></label>
            <input
              class="form-control"
              type="text" 
              v-model="name"
              name="name"
              id="invalidName" required
            />
            <small class="invalid-feedback">
              Skriv ett korrekt namn
            </small>
          </div>
          <div class="form-group">
            <label for="exampleFormControlInput1">Email address<span class="theme-color">*</span></label>
            <input
              class="form-control"
              v-model="email"
              name="email" 
              id="invalidEmail" required
            />
            <small class="invalid-feedback">
              Skriv en korrekt email address.
            </small>
          </div>
          <div class="form-group">
            <label for="exampleFormControlInput1">Telefonnummer</label>
            <input
              name="phone"
              type="text"
              v-model="phone"
              class="form-control"
              id="invalidPhone"
            />
            <small class="invalid-feedback">
              Skriv ett korrekt telefonnummer
            </small>
          </div>
          <div class="form-group">
            <label for="exampleFormControlTextarea1">Skriv ditt meddelande<span class="theme-color">*</span></label>
            <textarea
            class="form-control"
            name="message"
            v-model="message"
            cols="30" rows="8" required
            ></textarea>
          </div>
          <div class="row">
            <button type="submit" class="btn theme-bg text-white ml-3">
              Skicka
            </button>
            <div class="col-12 col-md-6 theme-color mt-3 mt-sm-0 d-none sentEmail" id="sentText">
              Ditt mail har skickats!
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';
export default {
    data() {
    return {
      name: '',
      email: '',
      phone: '',
      message: '',
      ValidEmail: false,
      ValidName: false,
      ValidPhone: false,
    }
  },
  methods: {
    sendEmail(e) {
      let nameElement = document.getElementById("invalidName")
      let emailElement = document.getElementById("invalidEmail")
      let phoneElement = document.getElementById("invalidPhone")
      let sentTextElement = document.getElementById("sentText")

      if(this.email.match(/^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/)) { 
        this.ValidEmail = true 
        emailElement.classList.remove("is-invalid")
      } else {
        emailElement.classList.add("is-invalid")
      }

      if(this.name.length > 1 && this.name.match(/^[a-zA-Z-,]+(\s{0,1}[a-zA-Z-, ])*$/)) { 
        this.ValidName = true 
        nameElement.classList.remove("is-invalid")
      } else {
        nameElement.classList.add("is-invalid")
      }

      if(this.phone.match(/^[0-9]+$/) && this.phone.length < 30) { 
        this.ValidPhone = true 
        phoneElement.classList.remove("is-invalid")
      } else {
        phoneElement.classList.add("is-invalid")
      }

      if(this.ValidName === true && this.ValidEmail === true && this.ValidPhone === true) {
        try {
          emailjs.sendForm('service_vvw6r3a', 'template_pzikc5s', e.target, 'user_6OBDttcckHAGVmgu5xM4r', {
            name: this.name,
            email: this.email,
            message: this.message,
            phone: this.phone
          })

          sentTextElement.classList.add("d-block")
          setTimeout(function(){
            sentTextElement.classList.remove('d-block');
          }, 10000)

        } catch (error) {
            console.log({error})
        }

        this.name = ''
        this.email = ''
        this.message = ''
        this.phone = ''
      } 
    },
  }
};
</script>

<style scoped>

.sentEmail {
  align-self: center;
}

.form-control:focus {
  border-color:#2979ff;
  box-shadow: 0px 1px 1px #2979ff inset, 0px 0px 8px #262c70;
}


textarea {
  resize: none;
}

hr {
  background: var(--theme-color);
  width: 5%;
  margin: auto;
  padding: 1px;
}

.btn {
  font-weight: 600;
  font-size: 14px;
  margin: 0;
}

a {
  text-decoration: none;
  color: white;
} a:hover {
  color: var(--theme-color) !important;
}


.custom-bg {
  background-color: white;
  padding: 20px;
  height: 160px;
  width: 160px !important;
  border-radius: 50px;
}

.my-text-size {
  font-weight: 500;
  margin-left: 5px;
  font-size: 16px;
  letter-spacing: 1px;
}

img {
  border-radius: 60px !important;
  max-height: 190px;
}

ul {
  list-style: none; 
}



</style>