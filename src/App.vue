<template>
  <div>
      <h2>Öğrencilerim</h2>
      
      <Student name="Sezer" phone="111" email="sss@hotmail.com" />
      <Student name="Seda" phone="222" email="sdsd@hotmail.com" />
      <Student name="Kevser" phone="333" email="kkk@hotmail.com" />
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


