<template>      
      <div id="intro"> 
        <div v-show="loadin == true"><!--loadin == true-->
          <div id="barSpacer"></div>
          <h5> loading ...</h5>
          <div id="myProgress">
            
            <div id="myBar"></div>
          </div>                              
          <div class="spacer"></div> 
          
          <img id="hue" alt="RIP Chester"  src="../assets/pictures/Chester-Linkin-Park.jpg">
                    
          <div id="megaSpacer"></div>
        </div>
      </div>
      <div class = "absol">
        <p class="verdanaBold">Some alt rock bands</p>
        <p>All right reserved to the photographs/labels.</p>   
        <div class="fun-font">
          <p>Jumpdaf*ckup!
            <img style="display: inline; margin: 45px;" alt="guitar" width="200px" height="auto" src="../assets/pictures/guitar2.png">
          </p>
        </div>
        <h2>Trapt</h2>
        <img  alt="Trapt" width="50%" height="auto" src="../assets/pictures/Trapt.jpg">
        <div class="spacer"></div>     
        <h2>Flyleaf</h2>
        <img  alt="Flyleaf" width="700px" height="auto" src="../assets/pictures/flyleaf.jpg">
        <div class="spacer"></div>
        <h2>Deftones</h2>
        <img  alt="Deftones" width="700px" height="auto" src="../assets/pictures/deftones_2001.jpg">
        <div class="spacer"></div>
        <h2>Taproot</h2>
        <img  alt="Taproot" width="700px" height="auto" src="../assets/pictures/Taproot-2023-Credit-Thom-Hazaert.jpg">
        <div class="spacer"></div>
        <h2>Head Phones President</h2>
        <img  alt="Head Phones President" width="820px" height="auto" src="../assets/pictures/headphonespresident.jpg">
        <div class="spacer"></div>
        <h2>LeVeL</h2>
        <img  alt="LeVeL" width="660px" height="auto" src="../assets/pictures/LeVeL.jpg">
        <div class="spacer"></div>
      </div>
      
    </template>
    <script>
    export default {
      name: 'Test_2',
      props: {
        
        myprop: Boolean 
      },
      data() {
            return {            
            i:0,
            loadin: true,
                        
            }
        },        
      watch: { 
        myprop: function(newVal, oldVal) { // watch it
          //console.log('Prop called load changed: ', newVal, ' | was: ', oldVal);
          this.mymove();
          
          setTimeout(() => this.loadin = !this.loadin, 3200);
          // toggle loadin 4000 ms here
        }
      },  
      methods: { 
         mymove() {
          if (this.i == 0) {
            this.i = 1;
            let elem = document.getElementById("myBar");
            let width = 1;
            let id = setInterval(frame, 30);
            function frame() {
              if (width >= 100) {
                this.loadin = true;
                //console.log("loadin is " + this.loadin);
                //console.log('clearinterval');                                                
                clearInterval(id);
                this.i = 0;
                
              } else {
                width++;
                elem.style.width = width + "%";
              }
            }
            
          }
          
        }
      }
    }
    </script>
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>
#myProgress {
  margin: auto;
  width: 40%;/*100%*/
  background-color: #ddd;
  border-radius: 10px;
}

#myBar {
  width: 1%;
  height: 30px;
  background-color: hsl(305, 11%, 55%);
  border-radius: 10px;
}
   
    #barSpacer{
      height: 150px;
    }
    #megaSpacer{
      height: 1000px;
    }
    
    div.absol{         
     /*position: absolute;*/
  margin-left: 6px;
  text-align: center;
 
  }
  #intro{
    /*margin: auto;*/
    text-align: center;
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
    #hue {
      filter: hue-rotate(200deg);
    }
    </style>