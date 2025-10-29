<template>
  <div>
      <form @submit.prevent="submitForm()">
            <div class="formControl">
                <label>Ad:</label>
                <input type="text" v-model="enteredName">
            </div>
            <div class="formControl">
                <label>Telefon:</label>
                <input type="tel" v-model="enteredPhone">
            </div>
            <div class="formControl">
                <label>E-mail:</label>
                <input type="email" v-model="enteredEmail">
            </div>
            <div class="formControl">
                <label>Ders Durumu:</label>
                <input type="checkbox" v-model="enteredIsPassed">
            </div>
            <div class="formControl">
                <button>Ekle</button>
            </div>
      </form>
      
  </div>
</template>


<script>

export default {
  name: 'student-form',
  emits:["addStudent"],
  data(){
    return{
       enteredName:'',
       enteredPhone:'',
       enteredEmail:'',
       enteredIsPassed:'',
    }
  },
  methods:{
      submitForm(){
        this.$emit('addStudent',this.enteredName,this.enteredPhone,this.enteredEmail,this.enteredIsPassed);
        this.enteredEmail='';
        this.enteredName='';
        this.enteredPhone='';
        this.enteredIsPassed=false;
      }
  }
  
}
</script>


