<template>
  <div class="centered-fixed">
    <div>
      <p class="verdanaHello" >Hello, I'm Even Becker</p>
      <p class="verdanaBold" >Welcome to my website</p>
      <p>made with 
        <img style="display: inline; margin: 0 5px;" alt="Vue logo" width="30px" height="auto" src="../assets/logo.svg">
        
      </p>
     
      
    </div>
    <!--<div class="white">
      <div id="spacerImg"></div>
      <img  alt="Mewtwo" width="200px" height="auto" src="../assets/pictures/Pokemon_Mewtwo.png">
      <div id="spacer"></div>
      <p>Genetic engineering is hazardous. <br> Mewtwo is too powerful to be placed in confinement.</p>
      <div id="spacerImg"></div>
    </div>-->
  <div id="mywhite" class="container-fluid p-5">
    <div id="carouselExampleControls" class="carousel carousel-dark slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div class="carousel-item active cimg" data-bs-interval="3000">
          <img src="../assets/pictures/Pokemon_Mewtwo.png" class="d-block" alt="Mewtwo">
          <div class="position-relative text-center"> 
            <p></p>           
            <p>Genetic engineering is hazardous. Mewtwo is too powerful to be placed in confinement.</p>
          </div>
        </div>
        <div class="carousel-item cimg">
          <img src="../assets/pictures/0144Articuno.png" class="d-block" alt="...">
          <div class="position-relative text-center">            
            <p></p><p>#144  Articuno </p>
            
          </div>
        </div>
        <div class="carousel-item cimg">
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

    text-align: center;
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