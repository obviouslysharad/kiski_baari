<template>
  <DisplayUser :name = "name" />
  <button @click = "onClick()">Find a person</button>
</template>

<script>
import DisplayUser from './components/DisplayUser.vue'

export default {
  name: 'App',
  components: {
    DisplayUser
  },
  methods:{
    onClick(){
      setTimeout(()=>{
        this.name = this.nameData[Math.floor(Math.random() * this.nameData.length)];
      },0);
    }
  },
  data(){
    return{nameData: ["Ajit Thapa","Akshay Maan","Akshita Khurana",
"Ashwani Sharma","Bikesh Kumar01","Chirag Khandelwal","Deepshi Sharma",
"Dinesh Samal","Ekta Srivastava","Himanshu Nigam","Jay Paliwal",
"Kanika Garg","Kunal Sharma","Mayank Goyal","Mohit Mehta","Nishtha Ghai",
"Piyush Dadhich","Piyush Sharma","Prachi Matta","Puneet Kumar Mahawar",
"Ram Singhal","Ravi Kumar","Rishabh Jain","Rishabh Kumawat","Sakshi Singhal","Shaminder Sekhon",
"Sharad Agarwal","Shashank Salaj","Shivam Pathak","Shivank Meena","Shivanshi Tripathi",
"Shobha Raghav","Shobhit Sharma","Subhash Nirwan","Subodh Sharma","Twinkle Jangid",
"Uttam Gupta","Vanshika Gandhi","Rishabh goel01","Vinita Agrawal", "Shilpa Sudhakar", "Akhilesh Tank", "Saneesh Ms"
 ], name:''}
  },
  created(){
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button{
    margin: 5px;
    padding: 5px;
    border-radius: 10px;
    border: none;
    box-shadow: 3px 3px 5px grey;
    
}
button:hover{
  background-color: red;
  transform: scale(1.1);
  transition: all .2s ease-in-out;

}
body{
  background-color:#444444;
}
</style>
