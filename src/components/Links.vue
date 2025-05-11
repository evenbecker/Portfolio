<template>
    <div class="centered-fixed">
             
      <h4 class="verdanaH">My Projects                    
      </h4>        
      <!--<div id="spacer"></div>-->
      <a href="https://even-audio-player.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A simple audio player
      </a>
      <p></p> 
      <a href="https://search-for-pkgs.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A prototype to search for Linux packages
        </a>
      <div id="spacer"></div>
     <h4 class="verdanaH">My Links                    
     </h4> 
     <a href="https://orcid.org/0000-0002-2004-9472" target="_blank"><i class="fa fa-external-link"></i>
      OrcID
        </a>
        <p></p>
     <a href="https://github.com/evenbecker" target="_blank"><i class="fa fa-github" style="font-size:36px"></i></a>

    </div>
  </template>
  <script>
      export default {
        name: 'Links',
        props: {
          msg: String
        }
      }
      </script>
      <!-- Add "scoped" attribute to limit CSS to this component only -->
      <style scoped>
    #spacer{
      height: 25px;
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
        color: black;
      }
      a:hover {
        color: #8E728B;
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