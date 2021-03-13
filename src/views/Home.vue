<template>
  <div class="app">
    <input type="text" v-model="text">
    <button @click="userClick">住所自動入力</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data(){
    return{
      text:""
    };
  },
  methods:{
    userClick(){
      this.text.push(
        
      )
    }
  }
}
</script>
