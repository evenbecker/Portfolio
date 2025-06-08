<template>
  <div class="centered-fixed">
    <div>
      <p class="verdanaHello" >Hello, I'm Even Becker</p>
      <p class="verdanaBold" >Welcome to my website</p>
              
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
            <p>Genetic engineering is hazardous. Mewtwo is too powerful to be placed in confinement.</p>
          </div>
        </div>
        <div class="carousel-item cimg" data-bs-interval="2000">
          <img src="../assets/pictures/0144Articuno.png" class="d-block" alt="...">
          <div class="position-relative text-center">            
            <p></p><p>#144  Articuno </p>
            
          </div>
        </div>
        <div class="carousel-item cimg" data-bs-interval="2000">
          <img src="../assets/pictures/0115Kangaskhan.png" class="d-block" alt="...">
          <div class="position-relative text-center">            
            <p></p><p>#115  Kangaskhan </p>
            
          </div>
        </div>
        <div class="carousel-item cimg" data-bs-interval="2000">
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
  <div id="phrase">
    <p id="phrasePadding">
        My theme is inspired by Mewtwo. I never looked beyond generation II because it has become inconsistent. It also represents humanity's peak, before people become slaved by their digital devices.       
      </p> 
  </div>
</div>
</template>
<script>
    export default {
      name: 'Test1',
      props: {
        msg: String
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
  .centered-fixed {
    /*position: fixed;
    z-index:1;
    top: 0;*/
    width:100%;
    text-align: center;
}
#phrase{
  margin-top: 1.5rem;
}
#phrasePadding{
  padding: 1rem 5rem;
  color: hsl(305, 11%, 32%);
}
    .white {
      background-color: white;
      left: 0;
      width:100%;
      /*min-height:400px;*/
      text-align: center;
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

    </style>