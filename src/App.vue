<template>
  <div id="app" class="container-fluid justify-content-center" :class="bg">
    <div class="modal" :class="{ 'modal-visible' : feature}">
      <div class="modal-content">
        <h3 class="text-center">
          Ask Swami Version 2.1.0 - 14 March release <br/>
          Feature Updates
          <svg @click="feature = false; modal = true" xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="red" class="bi bi-x-circle-fill cursor" viewBox="0 0 16 16">
            <path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM5.354 4.646a.5.5 0 1 0-.708.708L7.293 8l-2.647 2.646a.5.5 0 0 0 .708.708L8 8.707l2.646 2.647a.5.5 0 0 0 .708-.708L8.707 8l2.647-2.646a.5.5 0 0 0-.708-.708L8 7.293 5.354 4.646z"/>
          </svg>
        </h3>
        
        <br />
        <div class="row justify-content-center">
          <div class="col-lg-4 col-sm-12">
            <ol>
              <li>
                Adaptive Background
              </li>

              <li>
                Fixed typographic errors
              </li>

              <li>
                Adaptive Chit Images for some chits- Internet Required (still on beta)
              </li>

              <li>
                Fixed known bugs
              </li>
            </ol>
          </div>
        </div>

        <br />
        <div class="row justify-content-center">
          <div class="col-lg-4 col-sm-12">
            <div class="form-check">
              <input class="form-check-input" type="checkbox" v-model="check" @click="setStorage">
              <label class="form-check-label">
                Do not show again
              </label>
            </div>
          </div>
        </div>
      </div>
    </div>
    
    <div class="modal" :class="{ 'modal-visible' : modal}">
      <div class="modal-content text-center">
        <h3>Select</h3>
        
        <div class="row">
          <div class="col-6">
            <img id="f" @click="selectGender" class="cursor" src="@/assets/girl.jpg" height="150">
          </div>
          
          <div class="col-6">
            <img id="m" @click="selectGender" class="cursor" src="@/assets/boy1.jpg" height="150">
          </div>
        </div>
      </div>
    </div>

    <div class="modal" :class="{ 'modal-visible' : about}">
      <div class="modal-content text-center">
        <h3>
          About
          <svg @click="about = false" xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="red" class="bi bi-x-circle-fill cursor" viewBox="0 0 16 16">
            <path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM5.354 4.646a.5.5 0 1 0-.708.708L7.293 8l-2.647 2.646a.5.5 0 0 0 .708.708L8 8.707l2.646 2.647a.5.5 0 0 0 .708-.708L8.707 8l2.647-2.646a.5.5 0 0 0-.708-.708L8 7.293 5.354 4.646z"/>
          </svg>
        </h3>
        
        <div class="row">
          <div class="col">
            Made with <div class="heart" style="color: #e25555;">&hearts;</div> by MDH campus
          </div>
        </div>

        <br/>
        <div class="row">
          <div class="col">
            Fork or Pull @ 
            <a href="https://github.com/vigneshwaran-dev/Ask-Swami"  target="_blank" rel="noopener noreferrer">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-github" viewBox="0 0 16 16">
                <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
              </svg>
            </a>
          </div>
        </div>

        <br/>

        <div class="row">
          <div class="col-sm-12">
            Vigneshwaran
            <a href="https://vigneshwaran-dev.github.io/"  target="_blank" rel="noopener noreferrer">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-globe cursor" viewBox="0 0 16 16">
                <path d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm7.5-6.923c-.67.204-1.335.82-1.887 1.855A7.97 7.97 0 0 0 5.145 4H7.5V1.077zM4.09 4a9.267 9.267 0 0 1 .64-1.539 6.7 6.7 0 0 1 .597-.933A7.025 7.025 0 0 0 2.255 4H4.09zm-.582 3.5c.03-.877.138-1.718.312-2.5H1.674a6.958 6.958 0 0 0-.656 2.5h2.49zM4.847 5a12.5 12.5 0 0 0-.338 2.5H7.5V5H4.847zM8.5 5v2.5h2.99a12.495 12.495 0 0 0-.337-2.5H8.5zM4.51 8.5a12.5 12.5 0 0 0 .337 2.5H7.5V8.5H4.51zm3.99 0V11h2.653c.187-.765.306-1.608.338-2.5H8.5zM5.145 12c.138.386.295.744.468 1.068.552 1.035 1.218 1.65 1.887 1.855V12H5.145zm.182 2.472a6.696 6.696 0 0 1-.597-.933A9.268 9.268 0 0 1 4.09 12H2.255a7.024 7.024 0 0 0 3.072 2.472zM3.82 11a13.652 13.652 0 0 1-.312-2.5h-2.49c.062.89.291 1.733.656 2.5H3.82zm6.853 3.472A7.024 7.024 0 0 0 13.745 12H11.91a9.27 9.27 0 0 1-.64 1.539 6.688 6.688 0 0 1-.597.933zM8.5 12v2.923c.67-.204 1.335-.82 1.887-1.855.173-.324.33-.682.468-1.068H8.5zm3.68-1h2.146c.365-.767.594-1.61.656-2.5h-2.49a13.65 13.65 0 0 1-.312 2.5zm2.802-3.5a6.959 6.959 0 0 0-.656-2.5H12.18c.174.782.282 1.623.312 2.5h2.49zM11.27 2.461c.247.464.462.98.64 1.539h1.835a7.024 7.024 0 0 0-3.072-2.472c.218.284.418.598.597.933zM10.855 4a7.966 7.966 0 0 0-.468-1.068C9.835 1.897 9.17 1.282 8.5 1.077V4h2.355z"/>
              </svg>
            </a>
          </div>

          <div class="col-sm-12">
            K V Raghava
          </div>

          <div class="col-sm-12">
            Gaurav Rai
            <a href="https://www.instagram.com/gaurav__sampang/"  target="_blank" rel="noopener noreferrer">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-instagram cursor" viewBox="0 0 16 16">
                <path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"/>
              </svg>
            </a>
          </div>

          <div class="col-sm-12">
            M R Santhan
          </div>

          <div class="col-sm-12">
            B Mahesh
          </div>
        </div>

        <br />
        <div class="row">
          <p>
            For further improvements or suggestions please let us know by raising a issue on the repo.
          </p>
        </div>
      </div>
    </div>
    
    <div>
      <img class="rope" src='@/assets/rope.png'/>
      <div class="brick" />
      <img class="bell cursor" @click="ringBell" src="@/assets/bell.png"/>

      <audio id="bell"><source src="@/assets/bell.mp3" type="audio/mpeg"></audio>
      <audio id="gayathri" loop><source src="@/assets/sai_gayathri.mp3" type="audio/mpeg"></audio>
    </div>

    <div class="row align-items-center">
      <div class="col">
        <div class="card text-center">
          <div class="card-body">

            <img class="adaptive-image" v-if="onLine && image !== ''" :src="image">
            <br/>

            <h3 class="card-title">Swami says</h3>
            <br/>
            
            <h4 v-if="chit !== ''" class="card-text">"{{chit}}"</h4>
            <br/>

            <a class="btn btn-font" :class="bg" @click="pick">Pick</a>
          </div>
        </div>
      </div>
    </div>

    <div class="row footer-parent">
     <svg @click="about = true" xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="black" class="bi bi-info-circle-fill footer" viewBox="0 0 16 16">
      <path d="M8 16A8 8 0 1 0 8 0a8 8 0 0 0 0 16zm.93-9.412l-1 4.705c-.07.34.029.533.304.533.194 0 .487-.07.686-.246l-.088.416c-.287.346-.92.598-1.465.598-.703 0-1.002-.422-.808-1.319l.738-3.468c.064-.293.006-.399-.287-.47l-.451-.081.082-.381 2.29-.287zM8 5.5a1 1 0 1 1 0-2 1 1 0 0 1 0 2z"/>
    </svg>
    </div>
  </div>
</template>

<script>
import chits from '@/chits.json';

export default {
  name: "App",
  data() {
    return {
      backgrounds: [
        "blue-yellow",
        "orange-yellow",
        "purple-blue",
        "sky-bleu",
        "green-blue",
        "pink",
      ],
      bg: '',
      image: 'https://www.sathyasai.org/imageperfect/big/149.jpg',
      chit: 'Pick your chit',
      female: true,
      modal: false,
      about: false,
      feature: true,
      check: false,
      onLine:  navigator.onLine
    };
  },

  methods: {
    pick() {
      this.chit = '';
      this.ringBell();
      
      var number = Math.floor(Math.random() * (108 - 1 + 1) + 1);
      this.bg = chits[number - 1].bg;
      this.chit = chits[number - 1].txt;
      this.image = chits[number - 1].image;
    },

    ringBell(){
      document.getElementById('bell').volume = 0.5;
      document.getElementById('bell').play();
    },

    selectGender(e){
      if(e.target.id === 'm'){
        this.female = false;
        chits[53].txt = 'You are a good boy today';
      }

      this.modal = false;
      document.getElementById('gayathri').volume = 0.1;
      document.getElementById('gayathri').play();
    },

    setStorage(){
      if (this.check === false)
        localStorage.setItem('feature', true);
      else
        localStorage.removeItem('feature');
    },

    updateOnlineStatus(e){
      const { 
        type
      } = e;
      this.onLine = type === 'online';
    }
  },

  mounted() {
    window.addEventListener('online', this.updateOnlineStatus);
    window.addEventListener('offline', this.updateOnlineStatus);
  },

  beforeDestroy(){
    window.removeEventListener('online', this.updateOnlineStatus);
    window.removeEventListener('offline', this.updateOnlineStatus)
  },

  created() {
    if(localStorage.getItem('feature')) {
      this.feature = false;
      this.modal = true;
    }

    this.bg = this.backgrounds[
        Math.floor(Math.random() * this.backgrounds.length)
      ];
  },
};
</script>

<style lang="scss">
#app {
  color: #2c3e50;
  height: 100vh;
}

.blue-yellow {
  background-color: #52acff;
  background-image: linear-gradient(180deg, #52acff 25%, #ffe32c 100%);
}
.orange-yellow {
  background-color: #ffe53b;
  background-image: linear-gradient(147deg, #ffe53b 0%, #ff2525 74%);
}
.purple-blue {
  background-color: #21d4fd;
  background-image: linear-gradient(19deg, #21d4fd 0%, #b721ff 100%);
}
.sky-bleu {
  background-color: #8ec5fc;
  background-image: linear-gradient(62deg, #8ec5fc 0%, #e0c3fc 100%);
}
.green-blue {
  background-color: #fa8bff;
  background-image: linear-gradient(
    45deg,
    #fa8bff 0%,
    #2bd2ff 52%,
    #2bff88 90%
  );
}
.pink {
  background-color: #ffdee9;
  color: #ffdee9;
  background-image: linear-gradient(0deg, #ffdee9 0%, #b5fffc 100%);
}

.card{
  background: white;
  width: 60%;
  margin: 12% auto;
  padding: 10px;
}

@media (max-width: 767px) {
  .card {
    margin: 40% auto;
    width: 80%;
  }
}

.adaptive-image {
  max-width: 250px;
  max-height: 180px;
}

.btn-font{
  color: white;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgb(0,0,0);
  background-color: rgba(0,0,0,0.4);
}

.modal-visible {
  display: block;
}

.modal-content {
  background-color: #fefefe;
  margin: 15% auto; /* 15% from the top and centered */
  padding: 20px;
  width: 80%; /* Could be more or less, depending on screen size */
}

.heart {
	animation: beat .25s infinite alternate;
	transform-origin: center;
  display: inline-block;
}

@keyframes beat{
	to { transform: scale(1.4); }
}

.footer {
  margin-bottom: 20px;
  cursor: pointer;
}

.cursor {
  cursor: pointer;
}

// Bell
.rope{
  position: absolute;
  right:18px;
  height: 90px;
  top:-15px;
}

.brick {
  position:absolute;
  top:0px;
  right:0px;
  width:50px;
  border-top:15px solid brown;
}

.bell {
  position: absolute;
  right:0px;
  top:50px;
}

.bell:active{
  animation: shake 0.5s;
  animation-iteration-count: 1;
}

@keyframes shake {
  0% { transform:   rotate(15deg); }
  10% { transform:  rotate(-15deg); }
  20% { transform:  rotate(-15deg); }
  30% { transform:  rotate(15deg); }
  40% { transform:  rotate(15deg); }
  50% { transform:  rotate(-15deg); }
  60% { transform:  rotate(-15deg); }
  70% { transform:  rotate(15deg); }
  80% { transform:  rotate(15deg); }
}
</style>
