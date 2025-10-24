<template>
  <div>
      <h2>Öğrencilerim</h2>
      
      <Student v-for="student in students" :key="student.id" :name="student.name" :phone="student.phone" :email="student.email" :isPassed="student.isPassed"/>
      
    </div>
    
</template>

<script>
import Student from './components/Student.vue';
export default {
  name: 'App',
  components:{Student},
  data(){
    return{
      students:[
        {
          id:'1',
          name:"Sezer",
          phone:"111",
          email:"sss@hotmail.com",
          isPassed:true
        },
        {
          id:'2',
          name:"Seda",
          phone:"222",
          email:"sdsd@hotmail.com",
          isPassed:false
        },
        {
          id:'3',
          name:"Kevser",
          phone:"333",
          email:"kkk@hotmail.com",
          isPassed:false
        }

      ]
    }
  }
  
}
</script>


