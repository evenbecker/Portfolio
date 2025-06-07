<template>
    <div class="centered-fixed">
             
      <h4 class="verdanaH">My Projects                    
      </h4>        
      <!--<div id="spacer"></div>-->
      <span id="flashy2"> new!&nbsp;&nbsp;</span><a href="https://table-dragonball.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A table to use the Dragon Ball API
     </a>
      <p></p> 
      <a href="https://calendar-game.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A Calendar Game
      </a><a href="https://github.com/evenbecker/calendar-game" target="_blank">&nbsp;&nbsp;<i class="fa fa-info-circle myInfo"></i>       
      </a>
      <p></p> 
      <a href="https://even-pokemon-2001.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A Pokédex from 2001
      </a><a href="https://github.com/evenbecker/pokemon-2001" target="_blank">&nbsp;&nbsp;<i class="fa fa-info-circle myInfo"></i>       
      </a>
      <p></p> 
      <span id="flashy2"> new version!&nbsp;&nbsp;</span><a href="https://even-audio-player.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A simple audio player
      </a><a href="https://github.com/evenbecker/simple-audio-player" target="_blank">&nbsp;&nbsp;<i class="fa fa-info-circle myInfo"></i>       
      </a>
      <p></p> 
      <a href="https://search-for-pkgs.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
        A prototype to search for Linux packages
        </a><a href="https://github.com/evenbecker/search-for-pkgs" target="_blank">&nbsp;&nbsp;<i class="fa fa-info-circle myInfo"></i>       
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
        color: hsl(306, 11%, 44%);
      }
      i.myInfo {
        color: hsl(306, 11%, 44%);
        font-size:26px;
        
      }
      i.myInfo:hover {
        color: hsl(306, 11%, 30%);
      }

    .centered-fixed {
      /*position: fixed;
      z-index:1;
      top: 0;*/
  
      text-align: center;
  }
  #flashy2{
  color: #E0513B;
  font-size: 1.4em;
}
      
      </style>