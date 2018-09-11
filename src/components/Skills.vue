<template>
   
  <div class="skills">
    <div class="holder">
      Skills
      <ul>
        <li v-for="(data,index) in skills" :key='index'>{{index}}.{{data.skill}}</li>

        </ul>
        <!-- <div v-bind:class="{alert: showAlert,'another-class': showClass}"></div> -->
        <!-- <div v-bind:class="{alert: showAlert, 'another-class':showClass}"></div> -->
        <!-- <div v-bind:style="{ba}" -->
          <div v-bind:class="alertObject"></div>
    
  
   
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return{
      skills:[
        {"skill" :"Vue.js"},
        {"skill" :"Frontend Developer"}
      ],
      // showAlert: true
      alertObject: {
        alert: true,

      } 

      
      
    }
  },
  // props: {
    
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.alert {
  background-color: blue;
width: 100%;
height: 30px;
}
.another-class{
  border: 2px solid black;
}


 

</style>
