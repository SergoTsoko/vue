

<template>
 
 <div>
  <div class="number">
    <button @click="addNumber">+</button>
    <button v-on:click="removeNumber">-</button>

  </div>
  <div class="cifra">
    Ваша цифра: <em>{{ number }}</em> 
  </div>
  </div>
  <div>
    <div class="text1">
     
      {{text}}
      <button @click="hideText">скрыть текст</button>
      <button @click="showText">показать текст</button>
    </div>
  </div>
  
</template>

<script>
export default{
  data(){
    return {
      number: 0,
      text: "Тут написан очень важный текст"
    }
  },
  methods: {
    addNumber(){
      this.number += 1
    },
    removeNumber(){
      this.number -= 1
    },
    hideText(){
    this.text = ""
    },
    showText(){
      this.text = "тут написан очень важный текст"
    }
  }
}
</script>

<style scoped>
.number{
  margin-left: 40%;
  padding-top: 50px;

}
.cifra{
  margin-left: 40%;
  
}
.text1{
  margin-left: 40%;
}
</style>
