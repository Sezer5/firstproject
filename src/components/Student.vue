<template>
  <div>
      <!-- <h2>Öğrencilerim</h2>
      <ul v-for="student in students" :key="student.name">
        <li>{{student.name}}</li>
      </ul> -->
      Student Component
      Deneme
      <ul v-for="student in data" :key="student.name">
          <li>{{student.name}}</li>
      </ul>
      {{name}}
    </div>
</template>


<script>

export default {
  name: 'StudentInformation',
  props:[
    'name',
    'data'
  ],
  data(){
    return{
      
    }
  }
  
}
</script>


