<template>      
       
        <div id="intro" v-show="loadin == true"><!--loadin == true-->
          <div id="barSpacer"></div>
          <h5> loading ...</h5>
          <div id="myProgress">
            
            <div id="myBar"></div>
          </div>                              
          <div class="spacer"></div> 
          
          <img id="hue" alt="RIP Chester"  src="../assets/pictures/Chester-Linkin-Park.jpg">
                    
          <div id="megaSpacer"></div>
        </div>
      
      <div class = "absol">
        <p class="verdanaBold">Some alt rock bands</p>
        <p>All right reserved to the photographs/labels.</p>   
  
    <div class="section1">           
      <div class="animated_title">
        <div class="text_top">
          <div>
            <span class="text-bounce animate">Jumpdafuckup!</span>
            <!--<span class="text-bounce">guitar</span>-->
          </div>
        </div>      
      </div>
         
        <img class="guitar" alt="guitar" src="../assets/pictures/guitar2.png">
                         
    </div>                    
  
        <h2>Human Waste Project</h2>
        <img  alt="Human Waste Project" width="65%" height="auto" src="../assets/pictures/HumanWP.webp">
        <div class="spacer"></div>  
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
    .guitar{
      /*display: inline;*/
      position: absolute;
      z-index: 1;
      margin-left: 150px;
      /*width: 55px;*/
      height: 70px;

}
#myProgress {
  margin: auto;
  width: 40%;
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
    width: 100%;
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
      display: block;
      margin-left: auto;
      margin-right: auto;
    }



*::-webkit-scrollbar {
      width: 10px;
    }

    *::-webkit-scrollbar-track {
      background: whitesmoke;
    }

    *::-webkit-scrollbar-thumb {
      background: linear-gradient(90deg, rgba(120,120,121,1) 0%, rgba(136,136,136,1) 100%);
      border-radius: 10px;
    } 


    .section1 {
      font-family:'Poppins', sans-serif;
      display: flex;            
      position: relative;
      /*justify-content: center;
      align-items: center;*/
    }

    
    .animated_title {
      color: #222;
      font-family: 'Poppins', sans-serif;
      letter-spacing: 1.2px;
      height: 15vmax;
      position: relative;
      width: 33vmax;
      /*margin: 0 auto;*/
      display: flex;
      left: 40%;
      /*right: 20%;*/
      z-index: 2;
    }

    .animated_title > div {
      height: 85%;/*70% */
      overflow: hidden;
      position: absolute;
      width: 100%;
    }

    .animated_title > div div {
      font-size: 4vmax;
      font-weight: 580;
      padding: 2vmin 0;
      position: absolute;
      
    }

    .animated_title > div div span {
      display: block;
      
    }

    .animated_title > div.text_top {
      border-bottom: .8vmin solid #747474;
      width: 94%;
      animation: showBottomText 0.4s;
      animation-delay: 0.1s;
      top: 0;
    }

    .animated_title > div.text_top div {
      animation: showTopText 0.7s;
      animation-delay: 0.5s;
      animation-fill-mode: forwards;
      bottom: 0;
      transform: translate(0, 100%);
    }

    .animated_title > div.text_top div span:first-child {
      color: #747474;
    }

    .animated_title > div.text_top div span:first-child:hover{
      color: #F34F1C;
    }
    .animated_title > div.text_top div span:nth-child(2):hover{
      color: #FFBA01;
    }

   

    .bounce-in-right {
      animation: bounce-in-right 1.2s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
      animation-iteration-count: infinite;
    }

    .bounce-in-top {
      animation: bounce-in-top 1.3s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
      animation-iteration-count: infinite;
    }

    .bounce-in-left {
      animation: bounce-in-left 1.1s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
      animation-iteration-count: infinite;
    }

    .bounce-in-bottom {
      animation: bounce-in-bottom 1.2s cubic-bezier(0.455, 0.030, 0.515, 0.955) both;
      animation-iteration-count: infinite;
    }

    
    .text-bounce {
      transform: scaleY(1) translateY(0px);
      transform-origin: 50% 100%;
      transition: .3s ease-in-out;
    }
    .animate {
      animation: bouncy 1s infinite;/*forwards;*/
    }
    :hover {
      cursor: default;
    }

    @keyframes showTopText {
      0% {
        transform: translate3d(0, 100%, 0);
      }
      40%, 60% {
        transform: translate3d(0, 50%, 0);
      }
      100% {
        transform: translate3d(0, 0, 0);
      }
    }
    @keyframes showBottomText {
      0% {
        transform: translate3d(0, -100%, 0);
      }
      100% {
        transform: translate3d(0, 0, 0);
      }
    }

    @keyframes bouncy{
      0%{transform: scaleY(1) translateY(0px);}
      25%{transform: scaleY(.5) translateY(20px);}
      50%{transform: scaleY(1.1) translateY(-20px);}
      75%{transform: scaleY(.8) translateY(10px);}
      100%{transform: scaleY(1) translateY(0px);}
    }

    @keyframes bounce-in-right {
      0% {
        transform: translateX(120px);
        animation-timing-function: ease-in;
        opacity: 0;
      }
      38% {
        transform: translateX(0);
        animation-timing-function: ease-out;
        opacity: 1;
      }
      55% {
        transform: translateX(68px);
        animation-timing-function: ease-in;
      }
      72% {
        transform: translateX(0);
        animation-timing-function: ease-out;
      }
      81% {
        transform: translateX(32px);
        animation-timing-function: ease-in;
      }
      90% {
        transform: translateX(0);
        animation-timing-function: ease-out;
      }
      95% {
        transform: translateX(8px);
        animation-timing-function: ease-in;
      }
      100% {
        transform: translateX(0);
        animation-timing-function: ease-out;
      }
    }
    @keyframes bounce-in-top {
      0% {
        transform: translateY(-120px);
        animation-timing-function: ease-in;
        opacity: 0;
      }
      38% {
        transform: translateY(0);
        animation-timing-function: ease-out;
        opacity: 1;
      }
      55% {
        transform: translateY(-65px);
        animation-timing-function: ease-in;
      }
      72% {
        transform: translateY(0);
        animation-timing-function: ease-out;
      }
      81% {
        transform: translateY(-28px);
        animation-timing-function: ease-in;
      }
      90% {
        transform: translateY(0);
        animation-timing-function: ease-out;
      }
      95% {
        transform: translateY(-8px);
        animation-timing-function: ease-in;
      }
      100% {
        transform: translateY(0);
        animation-timing-function: ease-out;
      }
    }
    @keyframes bounce-in-left {
      0% {
        transform: translateX(-120px);
        animation-timing-function: ease-in;
        opacity: 0;
      }
      38% {
        transform: translateX(0);
        animation-timing-function: ease-out;
        opacity: 1;
      }
      55% {
        transform: translateX(-68px);
        animation-timing-function: ease-in;
      }
      72% {
        transform: translateX(0);
        animation-timing-function: ease-out;
      }
      81% {
        transform: translateX(-28px);
        animation-timing-function: ease-in;
      }
      90% {
        transform: translateX(0);
        animation-timing-function: ease-out;
      }
      95% {
        transform: translateX(-8px);
        animation-timing-function: ease-in;
      }
      100% {
        transform: translateX(0);
        animation-timing-function: ease-out;
      }
    }
    @keyframes bounce-in-bottom {
      0% {
        transform: translateY(120px);
        animation-timing-function: ease-in;
        opacity: 0;
      }
      38% {
        transform: translateY(0);
        animation-timing-function: ease-out;
        opacity: 1;
      }
      55% {
        transform: translateY(65px);
        animation-timing-function: ease-in;
      }
      72% {
        transform: translateY(0);
        animation-timing-function: ease-out;
      }
      81% {
        transform: translateY(28px);
        animation-timing-function: ease-in;
      }
      90% {
        transform: translateY(0);
        animation-timing-function: ease-out;
      }
      95% {
        transform: translateY(8px);
        animation-timing-function: ease-in;
      }
      100% {
        transform: translateY(0);
        animation-timing-function: ease-out;
      }
    }

    @keyframes image-bounce-in-right {
      0% {
        transform: translateX(0);
        opacity: 0;
      }
      38% {
        transform: translateX(10px);
        opacity: 1;
      }
      55% {
        transform: translateX(5px);
      }
      72% {
        transform: translateX(15px);
      }
      81% {
        transform: translateX(10px);
      }
      90% {
        transform: translateX(20px);
      }
      100% {
        transform: translateX(10px);
      }
    }

  

    </style>