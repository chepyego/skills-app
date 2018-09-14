<template>
<div class="container">

  <form @submit.prevent="addSkill">

  <input type="text" placeholder="Enter a skill you have.." v-model="skill">
  <input type="checkbox" id="checkbox" v-model="skill">
   <!-- {{skill}} -->
   <!-- <button type="submit">dg</button> -->
  </form>
   
  <div class="skills">
    <div class="holder">
      

      <ul>
        <li v-for="(data,index) in skills" :key='index'>{{data.skill}}</li>

        </ul>
        <p>These are the skills that you posses.</p>
        <!-- <div v-bind:class="{alert: showAlert,'another-class': showClass}"></div> -->
        <!-- <div v-bind:class="{alert: showAlert, 'another-class':showClass}"></div> -->
        <!-- <div v-bind:style="{ba}" -->
          <!-- <div v-bind:class="alertObject"></div> -->
          <!-- <div v-bind:style="{ backgroundColor: bgColor, width: bgWidth, height: bgHeight }"></div> -->
          <div v-bind:style="alertObject"></div>
    
  
   
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return{
      skill: '',
      skills:[
        {"skill" :"Vue.js"},
        {"skill" :"Frontend Developer"}
      ],
      // bgColor: 'blue',
      // bgWidth: '100%',
      // bgHeight: '30px'
      // // showAlert: true
      alertObject: {
        alert: true,

      },
       
    }
  },

  methods :{
    addSkill(){
      this.skills.push({skill: this.skill});
      this.skill = '';
    }

  } 
  // props: {
    
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* .alert {
  background-color: blue;
width: 100%;
height: 30px;
}
.another-class{
  border: 2px solid black;
} */
.holder{
  background: #ffffff
}
ul{
  margin:0;
  padding:o;
  list-style-type:none;
}
ul li{
  padding:20px;
  font-size: 1.3em;
  background-color: lightblue;
  border-left: 5px solid #000000 lightblue;
  margin-bottom: 2px;
 
}
p{
  text-align: center;
  padding: 30px 0;
  color: gray;
}
.container{
  box-shadow: 0px 0px lightgray;
}
input{
  width: calc(100% - 40px);
  border: 0;
  padding: 10px;
  font-size: 1.3em;
  background-color: #323333;
  color: #687F;
  margin-bottom: 4px;
  
  
}


 

</style>
