<template>
  <div id="app">
    <div class="split left">   
      <div id="left_side">
        <!--<p style="color:white; font-style:italic;">Github:</p>-->  
        <!--<a href="https://github.com/evenbecker" target="_blank"><i class="fa fa-github" style="font-size:36px"></i></a>-->
        
        <!--<p></p>-->
        <button @click="cmpnent ='Test1'">Home</button>
        <button @click="cmpnent ='Links'">Links </button>
        <button @click="cmpnent ='Todo1'">Todo list </button>
        <button @click="cmpnent ='Test_2'">Some alt rock bands</button>
        <button @click="cmpnent ='Bonus'">Bonus </button> 
        
        <div id="dna-container">
          <img id="dna" alt="dna" src="./assets/pictures/dna.png">
        </div>
      </div>    
     
    
    </div>
    <div class="split right">
      
      <Dynamic v-bind:cmpnent="cmpnent"></Dynamic>
    </div>
  </div>
</template>
  <script>
import Dynamic from './components/Dynamic.vue';
import Test1 from './components/Test1.vue'
import Test_2 from './components/Test2.vue'
import Todo1 from './components/Todo.vue'

  export default {
    name: 'app',
    
    components: {
    Test1, Todo1, Test_2, Dynamic
    },
    data() {
      return {
      cmpnent: "Test1",
      };
  }
  }
  </script>
<style>

  /*
#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
}
  */
#app {
  margin: 0 auto;
  /*min-width: 1680px;*/
  /*position: relative;*/
  font-family: 'Verdana', cursive;
  /*background-color: rgb(74, 180, 130);*/
  /*padding: 0;
  min-width: 925px;*/
}

/*
#app {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
*/
#dna-container{
  float:right;
  /*margin: 0 auto;*/
  /*background-color: rgb(74, 180, 130);*/
}

#dna{
  width:180px;
  border: 2px solid black; 
  margin-right: 28px;
  margin-top: 4px;
}
.split {
  height: 100%;
  width: 50%;
  position: fixed;
  z-index:1;
  top: 0;
  overflow-x: hidden;
  padding-top: 20px;
 
}

.left {
  left: 0;
  /*width: 30%;*/
  width:240px;
  /*max-width:280px;*/
  background-color: #000B21;
  /*background-color: rgb(67, 69, 72);*/
}
#left_side {
  left: 0;
  width: 100%;/*98% */
  height: 100%;
  /*text-align: center;*/
  font-weight: bold;
  background-color: #000B21;
}
 
.right {
  right: 0;
  float:left;
  /*width:fit-content;*/
  width: calc(100% - 240px);
  /*background-color: rgb(223, 238, 154);*/
  background-color: rgb(249, 246, 248);
}  
.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

button {
  border-radius: 0px;
  background-color: #6f596d; /* Green background */
  border: 3px solid #000B21; /* Green border */
  color: white; /* White text */
  padding: 0.6em 1.2em;
  cursor: pointer; /* Pointer/hand icon */
  width: 100%; /* Set a width if needed */
  display: block; /* Make the buttons appear below each other */
  white-space: nowrap; 
  min-width: auto;
  
  
}
/* Add a background color on hover */
button:hover {
  background-color: #AB87AC;
}
#spacer{
      height: 20px;
    }
/*
#github{
  padding: 0.0em 0.2em;
}*/
</style>