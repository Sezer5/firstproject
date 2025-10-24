<template>
  <div>
      <!-- <h2>Öğrencilerim</h2>
      <ul v-for="student in students" :key="student.name">
        <li>{{student.name}}</li>
      </ul> -->
     {{name}} {{studentIsPassed===true ? 'Geçti':'Kaldı'}} 
     <button @click="toggleDetail()">Bilgileri {{isVisible ? 'Sakla' : 'Göster'}}</button>
     <button @click="toggleIsPassed()">Öğrenci {{studentIsPassed===true ? 'Geçti' : 'Kaldı'}}</button>
      <ul v-if="isVisible">
          <li>{{phone}}</li>
          <li>{{email}}</li>
      </ul>
      
    </div>
</template>


<script>

export default {
  name: 'StudentInformation',
  // props:[
  //   'name',
  //   'phone',
  //   'email',
  //   'isPassed'
  // ],
  props:{
    name:{
      type:String,
      required:true,
    },
    phone:{
      type:String,
      required:true,
    },
    email:{
      type:String,
      required:true,
    },
    isPassed:{
      type:Boolean,
      required:false,
      default:false,
      // validator:function(value){
      //   return value === '1' || value==='0'
      // }
    }
  },  
  data(){
    return{
        isVisible:false,
        studentIsPassed:this.isPassed,
    }
  },
  methods:{
    toggleDetail(){
      this.isVisible=!this.isVisible;
    },
    toggleIsPassed(){
      
      this.studentIsPassed= !this.studentIsPassed;
     
        
    },
  }
  
}
</script>


