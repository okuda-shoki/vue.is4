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
    }
  },
  methods:{
 async created(){
   const item=await axios.get(
     'https://console.postcode-jp.com/key/rrwf6ibXcdcwxEr8poWbV0u6bp6FRNHRjQcqD3M=text=metric&aooid=rrwf6ibXcdcwxEr8poWbV0u6bp6FRNHRjQcqD3M'
   )
     this.text.push({text})
  }
  }
  };
</script>
