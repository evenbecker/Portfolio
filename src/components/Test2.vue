<template>
      <div class = "absol">
        <h1>Some alt rock bands</h1>
        <div class="fun-font">
          <p>Jumpdaf*ckup!
            <img style="display: inline; margin: 65px;" alt="guitar" width="200px" height="auto" src="../assets/pictures/guitar2.png">
          </p>
        </div>
        <h2>Flyleaf</h2>
        <img  alt="Flyleaf" width="700px" height="auto" src="../assets/pictures/flyleaf.jpg">
        <div id="spacer"></div>
        <h2>Deftones</h2>
        <img  alt="Deftones" width="700px" height="auto" src="../assets/pictures/deftones_2001.jpg">
        <div id="spacer"></div>
        <h2>Head Phones President</h2>
        <img  alt="Head Phones President" width="820px" height="auto" src="../assets/pictures/headphonespresident.jpg">
        <div id="spacer"></div>
        <h2>LeVeL</h2>
        <img  alt="LeVeL" width="660px" height="auto" src="../assets/pictures/LeVeL.jpg">
      </div>
    </template>
    <script>
    export default {
      name: 'Test_2',
      props: {
        msg: String
      }
    }
    </script>
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>
    #spacer{
      height: 40px;
    }
    div.absol{
      /*
     position: relative;
     top: 0;
     */
    
     position: absolute;
  margin-left: 6px;
  text-align: center;
  }
  .fun-font {
  font-family: 'Brush Script MT', cursive;
}
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
    </style>