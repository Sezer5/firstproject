<template>
  <div>
      <h2>Öğrencilerim</h2>
      
      <Student name="Sezer" phone="111" email="sss@hotmail.com" isPassed="1"/>
      <Student name="Seda" phone="222" email="sdsd@hotmail.com" isPassed="0"/>
      <Student name="Kevser" phone="333" email="kkk@hotmail.com" isPassed="0"/>
    </div>
    
</template>

<script>
import Student from './components/Student.vue';
export default {
  name: 'App',
  components:{Student},
  data(){
    return{
      
    }
  }
  
}
</script>


