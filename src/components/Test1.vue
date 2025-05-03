<template>
  <div class="centered-fixed">
    <div>
      <p class="verdanaHello" >Hello, I'm Even Becker</p>
      <p class="verdanaBold" >Welcome to my website</p>
      <p>made with 
        <img style="display: inline; margin: 0 5px;" alt="Vue logo" width="30px" height="auto" src="../assets/logo.svg">
        
      </p>
      <br>
      
    </div>
    <div class="white">
      <div id="spacerImg"></div>
      <img  alt="Mewtwo" width="200px" height="auto" src="../assets/pictures/Pokemon_Mewtwo.png">
      <div id="spacer"></div>
      <p>Genetic engineering is hazardous. <br> Mewtwo is too powerful to be placed in confinement.</p>
      <div id="spacerImg"></div>
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
    </style>