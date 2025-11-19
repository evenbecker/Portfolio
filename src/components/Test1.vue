<template>
  <div class="centered-fixed">
    <div>
      <div class="spacer"></div>
      <p class="verdanaHello">Hello, I'm Even Becker</p>

      <!--<p class="verdanaBold" >Welcome to my website</p>-->
      <div class="wave-container">
        <p class="wave-text simpleVerdanaBold">
          <span>W</span><span>e</span><span>l</span><span>c</span><span>o</span><span>m</span><span>e&nbsp;</span><span>t</span><span>o&nbsp;</span><span>m</span><span>y&nbsp;</span><span>w</span><span>e</span><span>b</span><span>s</span><span>i</span><span>t</span><span>e</span>
        </p>
      </div>
    </div>
    <div class="container my-5">
      <p class="verdanaHello mb-4">I have experience in the following web technologies:</p>
      <!-- <h1 class="text-center mb-4">title to remove</h1> -->
      <div class="row g-4">
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Angular.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Angular</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/React.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">React</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Vue.js.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Vue 3</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Bootstrap.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Bootstrap 5</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Material-UI.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Material UI</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Tailwind-CSS.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Tailwind-CSS</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/TypeScript.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">TypeScript</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Vite.js.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Vite</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Next.js.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Next.js</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Git.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Git</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/Java.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">Java</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/DotNetCoreLogoVector.svg.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">ASP.NET Core Web API</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-6 mb-4" style="max-width: 220px; min-width: 220px">
          <div class="logo-item">
            <img src="../assets/logos/PostgresSQL.png" alt=" ">
            <div class="logo-content">
              <p class="simpleVerdanaBold">PostgreSQL</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--
      <div id="spacerImg"></div>
    -->
    <div id="mywhite" class="container-fluid p-5 w-100">
      <div id="carouselExampleControls" class="carousel carousel-dark slide" data-bs-ride="true">
        <div class="carousel-inner">
          <div class="carousel-item active cimg" data-bs-interval="2000">
            <img src="../assets/pictures/Pokemon_Mewtwo.png" class="d-block" alt="Mewtwo">
            <div class="position-relative text-center">
              <p></p>
              <p class="purpleText">Genetic engineering is hazardous. Mewtwo is too powerful to be placed in
                confinement.</p>
            </div>
          </div>
          <div class="carousel-item cimg" data-bs-interval="2000">
            <img src="../assets/pictures/0144Articuno.png" class="d-block" alt="...">
            <div class="position-relative text-center">
              <p></p>
              <p>#144 Articuno </p>

            </div>
          </div>
          <div class="carousel-item cimg" data-bs-interval="3000">
            <img src="../assets/pictures/0115Kangaskhan.png" class="d-block" alt="...">
            <div class="position-relative text-center">
              <p></p>
              <p>#115 Kangaskhan </p>

            </div>
          </div>
          <div class="carousel-item cimg" data-bs-interval="3000">
            <img src="../assets/pictures/0123Scyther.png" class="d-block" alt="...">
            <div class="position-relative text-center">
              <p></p>
              <p>#123 Scyther </p>

            </div>
          </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls"
          data-bs-slide="prev">
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls"
          data-bs-slide="next">
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </div>
    <div class="widthText" id="phrase">
      <p class="purpleText">
        My theme is inspired by Mewtwo. I never looked beyond generation II because it has become inconsistent. It also
        represents humanity's peak, before people become slaved by their digital devices.
      </p>
    </div>
    <div class="spacer"></div>
  </div>
</template>
<script>
export default {
  name: 'Test1',
  props: {
    msg: String
  },
  mounted() {
    document.getElementById('app').scrollIntoView({ behavior: 'smooth' });
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

#phrase {
  margin-top: 1.5rem;
  padding: 1rem 0rem;
}

.purpleText {
  color: hsl(305, 11%, 24%);
}

p.pre {
  white-space: pre;
}

#spacerImg {
  height: 30px;
}

#mywhite {
  background-color: white;
}

.carousel-inner>.carousel-item>img {
  margin: auto;
}

.cimg img {
  width: auto;
  height: 345px;
  max-height: 345px;
}

/*Wave: */


.wave-text span {
  display: inline-block;
  /*font-size: 4rem;*/
  animation: wave 3.2s ease-in-out infinite;
  /*2s */
}

.wave-text span:nth-child(1) {
  animation-delay: 0s;
}

.wave-text span:nth-child(2) {
  animation-delay: 0.2s;
}

.wave-text span:nth-child(3) {
  animation-delay: 0.4s;
}

.wave-text span:nth-child(4) {
  animation-delay: 0.6s;
}

.wave-text span:nth-child(5) {
  animation-delay: 0.8s;
}

.wave-text span:nth-child(6) {
  animation-delay: 1.0s;
}

.wave-text span:nth-child(7) {
  animation-delay: 1.2s;
}

.wave-text span:nth-child(8) {
  animation-delay: 1.4s;
}

.wave-text span:nth-child(9) {
  animation-delay: 1.6s;
}

.wave-text span:nth-child(10) {
  animation-delay: 1.8s;
}

.wave-text span:nth-child(11) {
  animation-delay: 2.0s;
}

.wave-text span:nth-child(12) {
  animation-delay: 2.2s;
}

.wave-text span:nth-child(13) {
  animation-delay: 2.4s;
}

.wave-text span:nth-child(14) {
  animation-delay: 2.6s;
}

.wave-text span:nth-child(15) {
  animation-delay: 2.8s;
}

.wave-text span:nth-child(16) {
  animation-delay: 3.0s;
}

.wave-text span:nth-child(17) {
  animation-delay: 3.2s;
}

@keyframes wave {

  0%,
  100% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-10px);
    /*20px */
  }
}

.wave-container {
  margin-top: 2.5rem;
  margin-bottom: 1.5rem;
}

.logo-item {
  height: 11em;
  border-radius: 15px;
  border: 1px solid #74747468;
  background-color: white;
  overflow: hidden;
  position: relative;
  transition: transform 0.3s ease;
}

.logo-item:hover {
  transform: scale(1.05);
}



.logo-content {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  padding-bottom: 15px;
  padding-left: 15px;
  padding-right: 15px;
  /*background: rgba(0, 0, 0, 0.6);*/
  color: hsl(305, 11%, 24%);
  ;
}

.logo-item img {
  width: 5em;
  height: auto;
  padding-top: 1.5em;

}
</style>