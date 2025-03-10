<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="row p-0 m-0">
    <div class="col-1 p-0" style="margin-top: 20%;">
      <img src="/img/left-arrow-png-file-2608997235.png" alt="" v-if="i>0" v-on:click="prevpage()">
    </div>
    <div class="col-10 p-0"> 
      <img src="/img/page000.png" alt="" v-if="i==0"> 
      <img src="/img/page001.png" alt="" v-if="i==1"> 
      <img src="/img/page002.png" alt="" v-if="i==2"> 
      <img src="/img/page003.png" alt="" v-if="i==3"> 
      <img src="/img/page004.png" alt="" v-if="i==4"> 
      <img src="/img/page005.png" alt="" v-if="i==5"> 
      <img src="/img/page006.png" alt="" v-if="i==6"> 
      <img src="/img/page007.png" alt="" v-if="i==7"> 
      <img src="/img/page008.png" alt="" v-if="i==8"> 
      <img src="/img/page009.png" alt="" v-if="i==9"> 
      <img src="/img/page010.png" alt="" v-if="i==10"> 
      <img src="/img/page011.png" alt="" v-if="i==11"> 
      <img src="/img/page012.png" alt="" v-if="i==12"> 
      <img src="/img/page013.png" alt="" v-if="i==13"> 
      <img src="/img/page014.png" alt="" v-if="i==14"> 
      <img src="/img/page015.png" alt="" v-if="i==15"> 
    </div>
    <div class="col-1 p-0" style="margin-top: 20%;">
      <img src="/img/arrow-symbol-arrow-transparent-png-image--34-3464602881.png" alt="" v-if="i<15" v-on:click="nextpage()">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    var self = this;
        return {
          i: 0,
          disabled: false,
          abled:false,
          quizz:true,
          reponse:false,
          warn: false,
          idletime: 0,
          idlewarn(){self.warn = true},

        }
    },
    methods: {
      prevpage() {
      var that = this
      if(that.i > 0){
      that.i -= 1
    } },
    nextpage() {
      var that = this
      if(that.i < 15){
      that.i += 1
    }
    },
}
  }

</script>

<style scoped>
</style>
