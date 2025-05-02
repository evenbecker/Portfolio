<template>
    
    <!--<p>The dynamic component prints : {{cmpnent}}</p>-->
    <div class="korn" v-if="cmpnent=='Todo1'">
        <!--<p>The v-if Todo1 works</p>-->
        <Todo1></Todo1>
    </div>
    <div v-if="cmpnent=='Test1'">
        <!--<p>The v-if Test1 works</p>-->
       <Test1></Test1>
    </div>
    <div v-if="cmpnent=='Test_2'">
        <!--<p>The v-if Test_2 works</p>-->
        <Test_2></Test_2>
    </div>
    <div v-if="cmpnent=='Links'">
        <!--<p>The v-if Bonus works</p>-->
        <Links></Links>
    </div>
    <div v-if="cmpnent=='Bonus'">
        <!--<p>The v-if Bonus works</p>-->
        <Bonus></Bonus>
    </div>
</template>  
<script>
import Test1 from './Test1.vue'
import Test_2 from './Test2.vue'
import Todo1 from './Todo.vue'
import Bonus from './Bonus.vue'
import Links from './Links.vue'
    export default {
      name: 'Dynamic',
      components: {
        Test1,Test_2,Todo1,Bonus,Links
  },
      props: ['cmpnent'],
    }

</script>
<style scoped>
.korn {
    margin-left: 30px;
    margin-right: 50px;
    margin-top: 20px;
    /*background-color: gold;*/
    max-width: 450px; 
  }
</style>