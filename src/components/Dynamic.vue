<template>
    
    <!--<p>The dynamic component prints : {{cmpnent}}</p>-->
    <div class="korn mytop" v-if="cmpnent=='Todo1'">
        <!--<p>The v-if Todo1 works</p>-->
        <Todo1></Todo1>
    </div>
    <div class="mytop" v-if="cmpnent=='Test1'">
        <!--<p>The v-if Test1 works</p>-->
       <Test1></Test1>
    </div>
    <div v-if="cmpnent=='Test_2'">
        <!--<p>The v-if Test_2 works</p>-->
        <Test_2 :myprop="load"></Test_2>
       <!-- < this.load = !this.load>-->
    </div>
    <div v-if="cmpnent=='Links'">
        
        <Links></Links>
    </div>
    <div v-if="cmpnent=='Bonus'">
        <!--<p>The v-if Bonus works</p>-->
        <Bonus></Bonus>
    </div>
    <div class="likeFlex mytop" v-if="cmpnent=='Validation'">
        
        <Validation></Validation>
    </div>
</template>  
<script>
import Test1 from './Test1.vue'
import Test_2 from './Test2.vue'
import Todo1 from './Todo.vue'
import Bonus from './Bonus.vue'
import Links from './Links.vue'
import Validation from './Validation.vue'

export default {
      name: 'Dynamic',
      components: {
        Test1,Test_2,Todo1,Bonus,Links,Validation
  },
      props: ['cmpnent'],
      data () {
        return {
            load: true,
            
        }
    },
    watch: { cmpnent: function(newVal, oldVal) { // watch it
        //console.log('Prop called cmpnent: changed: ', newVal, ' | was: ', oldVal);
        if (newVal == "Test_2"){
            setTimeout(() => this.load = !this.load, 200);
            //this.load = !this.load;
           
        }        
        }                        
    }
}
</script>
<style scoped>
.korn {
    min-width: 410px;
    max-width: 450px; 
    position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
    /*
    text-align: center;
    margin-left: 90px;
    margin-right: 150px;
    margin-top: 20px;
    background-color: gold;
    max-width: 450px; 
    */
  }
.likeFlex{
    margin: 0 auto;
    padding: 2rem;
  display: flex;
  flex-direction: column;
  background-color: #FAFAFF;
  place-items: center;
}  
.mytop{
    padding-top: 20px;
}
</style>