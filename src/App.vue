<template>
  <div>
      <StudentForm />
      
      <div class="mainContent">
            <h2>Öğrencilerim</h2>
            <Student v-for="student in students" :key="student.id" :id="student.id" :name="student.name" :phone="student.phone" :email="student.email" :isPassed="student.isPassed"
            @toggleStudentIsPassed="toogleStudentstatus"
          />
      </div>
      
      
    </div>
    
</template>

<script>
import Student from './components/Student.vue'
import StudentForm from './components/StudentForm.vue'
export default {
  name: 'App',
  components:{Student,StudentForm},
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
    
  },
  methods:{
      toogleStudentstatus(studentId){
          console.log(studentId);
          const myStudent = this.students.find((student)=>student.id === studentId);
          myStudent.isPassed=!myStudent.isPassed;
      },
    }
}
</script>
<style>
    *{
      box-sizing: border-box;
      margin: 0px;
      padding: 0px;
    }
    form{
    box-shadow: rgba(6, 24, 44, 0.4) 0px 0px 0px 2px, rgba(6, 24, 44, 0.65) 0px 4px 6px -1px, rgba(255, 255, 255, 0.08) 0px 1px 0px inset;
    max-width: 600px;
    width: 100%;
    margin: 10px auto;
    border-radius: 20px;
    text-align: center;
    padding: 20px;

  }
  form input{
    width: 100%;
    padding: 5px;
    border-radius: 10px;
  }
  .formControl{
      margin: 20px;
  }

  .formControl label{
      font-weight: bold;
      font-size: 20px;
  }
  .mainContent{
    box-shadow: rgba(6, 24, 44, 0.4) 0px 0px 0px 2px, rgba(6, 24, 44, 0.65) 0px 4px 6px -1px, rgba(255, 255, 255, 0.08) 0px 1px 0px inset;
    max-width: 600px;
    width: 100%;
    margin: 10px auto;
    border-radius: 20px;
    text-align: center;
    padding: 20px;
  }

  .mainContent button{
    background-color: green;
    color: white;
    margin: 10px;
    padding: 10px;
    border-radius: 10px;
    border: none;
    cursor: pointer;
  }
  ul{
    list-style-type: none;
  }
</style>

