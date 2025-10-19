<template>
  <div>
      <h2>Öğrencilerim</h2>
      <ul v-for="student in students" :key="student.name">
        <li>{{student.name}}</li>
      </ul>
      
    </div>
    <Student :data="students" name="Can"/>
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
          name:'Sezer',
          phone:'123',
        },
        {
          name:'Seda',
          phone:'123',
        },
         {
          name:'Kevser',
          phone:'123',
        },
        ]
    }
  }
  
}
</script>


