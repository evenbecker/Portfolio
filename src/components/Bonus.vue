<template>
    <div class="centered-fixed">
      <div>
        
        <p>made with 
          <img style="display: inline; margin: 0 5px;" alt="Vue logo" width="30px" height="auto" src="../assets/logo.svg">
          
        </p>
        <p>under construction</p>
      </div>
     
    </div>
  </template>
  <script>
      export default {
        name: 'Bonus',
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
        text-align: center;
      }
      </style>