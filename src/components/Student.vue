<template>
  <div>
      <!-- <h2>Öğrencilerim</h2>
      <ul v-for="student in students" :key="student.name">
        <li>{{student.name}}</li>
      </ul> -->
     {{name}}  <button @click="toggleDetail()">Bilgileri {{isVisible ? 'Sakla' : 'Göster'}}</button>
      <ul v-if="isVisible">
          <li>{{phone}}</li>
          <li>{{email}}</li>
      </ul>
      
    </div>
</template>


<script>

export default {
  name: 'StudentInformation',
  props:[
    'name',
    'phone',
    'email'
  ],
  data(){
    return{
        isVisible:false,
    }
  },
  methods:{
    toggleDetail(){
      this.isVisible=!this.isVisible;
    }
  }
  
}
</script>


