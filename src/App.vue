<template>
  <div id="app">
    
      <div class="row default-container g-0">
    <div id="menu-col" class="col-2">   
      <div id="dark-menu">
        <!--<p style="color:white; font-style:italic;">Github:</p>-->  
        <!--<a href="https://github.com/evenbecker" target="_blank"><i class="fa fa-github" style="font-size:36px"></i></a>-->
        <div id="spacer"></div>
        <!--<p></p>-->
        <div id="group">
        <button class="mybutton" @click="cmpnent ='Test1'">Home</button>
        <button class="mybutton" @click="cmpnent ='Links'">Projects </button>
        <button class="mybutton" @click="cmpnent ='Validation'">Form validation  </button>
        <button class="mybutton" @click="cmpnent ='Todo1'">Todo list </button>
        <button class="mybutton" @click="cmpnent ='Test_2'"> Alt rock bands</button>
        <button class="mybutton" @click="cmpnent ='Bonus'">Linux </button>   
        </div>
                   
        <img class="img-responsive" id="dna" alt="dna" src="./assets/pictures/hexagon.jpg">       
      </div>
    </div>    
                 
    <div class="col-10 mybcolor">
      
      <Dynamic v-bind:cmpnent="cmpnent"></Dynamic>
    </div>
    </div>
  
  <div id="footer">
    <p>made with 
        <img style="display: inline; margin: 0 3px;" alt="Vue logo" width="26px" height="auto" src="./assets/logo.svg">
        
      </p>
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
  /*margin: 0 auto;*/   
 
  font-family: 'Verdana', cursive;
 
}
/*
#app {
    display: flex;
      font-family: 'Verdana', cursive;
    
    justify-content: center;
    align-items: center;
  }
*/
#dna{
  opacity: 0.5;   
    width: 100%;
    object-fit: cover;    
    filter: hue-rotate(246deg); 
}
.left {
  flex: 20%;
  /*max-width:280px;*/
  background-color: #3a2f44;
  background-color: rgb(249, 246, 248);
  /*background-color: rgb(67, 69, 72);*/
} 


.mybutton {
  width: 100%;
  border-radius: 0px;
  background-color: hsl(305, 11%, 39%);   
  border: 3px solid #3a2f44; 
  color: white; /* White text */
  padding: 0.6em 1.2em;
  cursor: pointer; /* Pointer/hand icon */ 
  position: relative;
  overflow: hidden;      
}
#bidon{
  color:hsl(305, 11%, 39%); /* 111,89,109 */
  background: rgba( 111, 89 , 109, 1 );
}
/* Add a background color on hover */
.mybutton:hover {
  background-color: #3a2f44;/*hsl(305, 11%, 55%);*/
  /*background-image: linear-gradient(to right, hsl(305, 11%, 65%), hsl(305, 11%, 39%) );*/ 
  transition: 700ms;
}

.mybutton:after {
  content: "";
  background: hsl(305, 11%, 65%);
  display: block;
  position: absolute;
  padding-top: 300%;
  padding-left: 350%;
  margin-left: -20px!important;
  margin-top: -120%;
  opacity: 0;
  transition: all 1.0s
}
.mybcolor{
  background-color: rgb(249, 246, 248);
}
.mybutton:active:after {
  padding: 0;
  margin: 0;
  opacity: 1;
  transition: 0s
}  
#flashy{
  color: hsl(12, 87%, 82%);
  font-size: 1.4em;
}
.flashy{
  padding: 0.4em 1.2em;
}
#spacer{
      height: 20px;
    }
/*
#dark-menu{
  background-color: #3a2f44;
  width:100%;
  margin-right: -1.5rem;
}
*/
#dark-menu{
  background-color: #3a2f44;
  width:100%;
  /*margin-left: 0.75rem;
  margin-right: 0.75rem;*/
}
#menu-col{
  background-color: #3a2f44;
}    
#group{
  margin-bottom: 1rem;
}
/*
#github{
  padding: 0.0em 0.2em;
}*/
.default-container {
    background: #c4dffa;
    padding: 0px 0px;
    min-height: 97vh;
    overflow-y: auto;
    display: flex;
    /*justify-content: center;
    align-items: center;*/
}
#footer{
  width:100%;
  min-height: 3vh;
  display: flex;
  justify-content: center;
  color: hsl(0, 0%, 90%);
  background-color: hsl(305, 11%, 39%);
}
#footer > p {
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}
</style>