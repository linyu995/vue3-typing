<template>
  <div class="hello">
    <div id="na">花元宝</div>
  </div>
</template>
<script>
import {defineComponent,onMounted} from 'vue'
import {f1} from '../utils/globalLib/globalexample'
import {a} from "../utils/moduleLib/moduleexample";
import {jqueryDemo} from '../utils/UMDLib/globalUMD/globalJquery'

const demo=defineComponent({
   setup(){
     onMounted(()=>{
       console.log("全局"+f1())
       console.log("模块"+a);
       jqueryDemo("na")  //全局jquery
     })
   }
 })
  export default demo
</script>
<style scoped>

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
<style type="text/css">
  .blue {
    color:blue;
  }
</style>
