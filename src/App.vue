<template>
  <div>
      <h2>Öğrencilerim</h2>
      <ul v-for="student in students" :key="student.name">
        <li>{{student.name}}</li>
      </ul>
    </div>
</template>

<script>

export default {
  name: 'App',
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


