<template>
  <div class="centered-fixed">

    <h4 class="verdanaH">My Projects
    </h4>
    <!--<div id="spacer"></div>-->
    <span id="flashy2"> new!&nbsp;&nbsp;</span><a href="https://pokemon-gen2.netlify.app/" target="_blank"><i
        class="fa fa-external-link"></i>
      Pokémon Gen II: A Nostalgia Project
    </a><a href="https://github.com/evenbecker/pokemon-gen2" target="_blank">&nbsp;&nbsp;<i
        class="fa fa-info-circle myInfo" data-bs-toggle="tooltip" data-bs-placement="right"
        title="click to read the project's description on Github"></i>
    </a>
    <p></p>

    <a href="https://github.com/evenbecker/App-for-ordering-food" target="_blank"><i class="fa fa-external-link"></i>
      An app for ordering food
    </a>
    <p></p>
    <a href="https://init-freedom.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
      A responsive website about init freedom
    </a><a href="https://github.com/evenbecker/search-for-pkgs" target="_blank">&nbsp;&nbsp;<i
        class="fa fa-info-circle myInfo" data-bs-toggle="tooltip" data-bs-placement="right"
        title="click to read the project's description on Github"></i>
    </a>
    <p></p>
    <a href="https://github.com/evenbecker/Initial-D-App" target="_blank"><i class="fa fa-external-link"></i>
      The Initial D Cars App
    </a>
    <p></p>

    <a href="https://table-dragon-ball.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
      A table to use the Dragon Ball API
    </a><a href="https://github.com/evenbecker/table-dragon-ball-api" target="_blank">&nbsp;&nbsp;<i
        class="fa fa-info-circle myInfo" data-bs-toggle="tooltip" data-bs-placement="right"
        title="click to read the project's description on Github"></i>
    </a>
    <p></p>



    <a href="https://even-audio-player.netlify.app/" target="_blank"><i class="fa fa-external-link"></i>
      A simple audio player
    </a><a href="https://github.com/evenbecker/simple-audio-player" target="_blank">&nbsp;&nbsp;<i
        class="fa fa-info-circle myInfo" data-bs-toggle="tooltip" data-bs-placement="bottom"
        title="click to read the project's description on Github"></i>
    </a>


    <hr>

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
  },
  mounted() {
    var tooltipTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'))
    var tooltipList = tooltipTriggerList.map(function (tooltipTriggerEl) {
      return new bootstrap.Tooltip(tooltipTriggerEl)
    })
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#spacer {
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
  color: hsl(305, 32%, 44%);
}

i.myInfo {
  color: hsl(305, 32%, 44%);
  font-size: 26px;
  vertical-align: middle;
}

i.myInfo:hover {
  color: hsl(305, 32%, 30%);
}


#flashy2 {
  color: #E0513B;
  font-size: 1.4em;
}

hr {
  margin-top: 2rem;
  margin-bottom: 2rem;
}
</style>