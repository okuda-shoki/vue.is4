<template>
  <div class="home">
    <input type="text" v-model="text">
    <button @click="created">住所自動入力</button>
    <p>Address:{{message}}</p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data(){
    return{
      text:"",
      message:""
    }
  },
  methods:{
 async created(){
   const item=await axios.get(
     'https://apis.postcode-jp.com/api/v4/postcodes/${this.text}?&apiKey=6AjrKzT1WvbemsWutv7otk8aU2LyRDObIMW4p0q'
   )
   console.log(item);
   this.message=item.data[0].allAddress;
  },
}, 
}
</script>