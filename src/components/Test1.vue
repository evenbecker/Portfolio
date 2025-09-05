<template>
  <div class="centered-fixed">
    <div>
      <p class="verdanaHello" >Hello, I'm Even Becker</p>

      <!--<p class="verdanaBold" >Welcome to my website</p>-->
      <div class="wave-container">
    <p class="wave-text simpleVerdanaBold">
        <span>W</span><span>e</span><span>l</span><span>c</span><span>o</span><span>m</span><span>e&nbsp;</span><span>t</span><span>o&nbsp;</span><span>m</span><span>y&nbsp;</span><span>w</span><span>e</span><span>b</span><span>s</span><span>i</span><span>t</span><span>e</span>
    </p>
</div>        
    </div>
    <!--
      <div id="spacerImg"></div>
    -->
  <div id="mywhite" class="container-fluid p-5 w-100">
    <div id="carouselExampleControls" class="carousel carousel-dark slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active cimg" data-bs-interval="2000">
          <img src="../assets/pictures/Pokemon_Mewtwo.png" class="d-block" alt="Mewtwo">
          <div class="position-relative text-center"> 
            <p></p>           
            <p class="purpleText">Genetic engineering is hazardous. Mewtwo is too powerful to be placed in confinement.</p>
          </div>
        </div>
        <div class="carousel-item cimg" data-bs-interval="2000">
          <img src="../assets/pictures/0144Articuno.png" class="d-block" alt="...">
          <div class="position-relative text-center">            
            <p></p><p>#144  Articuno </p>
            
          </div>
        </div>
        <div class="carousel-item cimg" data-bs-interval="3000">
          <img src="../assets/pictures/0115Kangaskhan.png" class="d-block" alt="...">
          <div class="position-relative text-center">            
            <p></p><p>#115  Kangaskhan </p>
            
          </div>
        </div>
        <div class="carousel-item cimg" data-bs-interval="3000">
          <img src="../assets/pictures/0123Scyther.png" class="d-block" alt="...">
          <div class="position-relative text-center">            
            <p></p><p>#123  Scyther </p>
            
          </div>
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
  <div class="widthText" id="phrase">
    <p class="purpleText">
        My theme is inspired by Mewtwo. I never looked beyond generation II because it has become inconsistent. It also represents humanity's peak, before people become slaved by their digital devices.       
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

#phrase{
  margin-top: 1.5rem;
  padding: 1rem 0rem;
}

.purpleText{
  color: hsl(305, 11%, 24%);
}
   
    p.pre {
  white-space: pre;
    }
    #spacerImg{
      height: 30px;
    }
   #mywhite{
    background-color: white;
   }
    .carousel-inner > .carousel-item > img{ margin:auto; }

    .cimg img {
width: auto;
height: 345px;
max-height: 345px;
}
/*Wave: */


.wave-text span {
    display: inline-block;
    /*font-size: 4rem;*/
    animation: wave 3.2s ease-in-out infinite;/*2s */
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
    0%, 100% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(-10px);/*20px */
    }
}
.wave-container{
  margin-top: 2.5rem;
  margin-bottom: 1.5rem;
}
    </style>