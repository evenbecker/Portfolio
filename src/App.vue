<template>
  <div id="app">
    <nav class="navbar navbar-expand-sm navbar-custom fixed-top">  
  <div class="container-fluid">
    <!-- Links -->
    <div class="enlarge" >
      <ul class="navbar-nav">
        <li class="nav-item">
          <button class="nav-button" @click="cmpnent ='Test1'">Home</button>
        </li>
        <li class="nav-item">
          <button class="nav-button" @click="cmpnent ='Links'">Projects </button>
        </li>
        <li class="nav-item">
          <button class="nav-button" @click="cmpnent ='Validation'">Experiments  </button> 
        </li>
        <li class="nav-item">
          <button class="nav-button" @click="cmpnent ='Todo1'">Todo list </button> 
        </li>
        <li class="nav-item">
          <button class="nav-button" @click="cmpnent ='Bonus'">Linux </button>   
        </li>
        <li class="nav-item">
          <button class="nav-button" @click="cmpnent ='Test_2'"> Alt rock bands</button>  
        </li>
      </ul>
    </div>
  </div>

</nav>
    <div class="row default-container g-0 mybcolor">
      <div id="spacerNav"></div>                        
      <div class="col-12 ">
      
      <Dynamic v-bind:cmpnent="cmpnent"></Dynamic>
    </div>
  </div>
  
  <div id="footer">
    <p>&copy;  {{currentYear }} | Developed by Even Becker. 
      <!--<img style="display: inline; margin: 0 3px;" alt="Vue logo" width="22px" height="auto" src="./assets/logo.svg">
    -->
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
      currentYear: '',
      };
  },
  mounted() {
        this.year();
    },
  methods: { 
    year() {
      this.currentYear = new Date().getFullYear().toString();
    }
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


.nav-button{
  height: 100%;
  background-color: hsl(305, 11%, 43%); 
  color: hsl(0, 0%, 96%);
  padding: 0 2.2em;
  border: none;
  padding: 0.4em 2em;
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
.nav-button:hover {
  background-color: hsla(302, 21%, 62%, 0.75);/*hsl(305, 11%, 55%);*/
  /*background-image: linear-gradient(to right, hsl(305, 11%, 65%), hsl(305, 11%, 39%) );*/ 
  transition: 400ms;
  color: white;
}
/*
.nav-button:visited{
  background-color: purple; 
  color: hsl(0, 0%, 96%);
}*/
.nav-button:focus{
  background-color: hsla(302, 21%, 62%, 0.75);
  color: hsl(0, 0%, 96%);
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

.default-container {
    
    padding: 0px 0px;
    min-height: 96vh;/* 95.6vh; */
    overflow-y: auto;
    display: flex;
    /*justify-content: center;
    align-items: center;*/
}
#footer{
  width:100%;
  /*min-height: 2vh;*/
  display: flex;
  padding: 0.175rem 0;
  justify-content: center;
  align-items: center;
  color: hsl(0, 0%, 96%);
  background-color: hsl(305, 11%, 43%);
}

#footer > p {
  margin-top: 0.25rem;
  margin-bottom: 0.6rem;
  font-size: 0.85rem;
}
.navbar-custom {
    background-color: hsl(305, 11%, 43%);;
}
.navbar-custom .navbar-brand,
 .navbar-custom .navbar-text {
     color: hsl(0, 0%, 96%);
 }
 .enlarge{
  margin-bottom : -8px;
  margin-top : -8px;
 }
 #spacerNav{
  height: 20px;
 }
</style>