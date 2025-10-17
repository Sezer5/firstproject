<template>
  <div>
      <!-- <h2>Öğrencilerim</h2>
      <ul v-for="student in students" :key="student.name">
        <li>{{student.name}}</li>
      </ul> -->
      Student Component
      Deneme
    </div>
</template>

<script>

export default {
  name: 'StudentInformation',
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


