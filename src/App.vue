<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="row p-0 m-0 page">
    <div class="col-1 p-0 my-auto" style="cursor: pointer;">
      <img src="/img/left-arrow-png-file-2608997235.png" alt="" v-if="i>0" v-on:click="prevpage()">
    </div>
    <div class="col-10 p-0 my-auto grille"> 
      <img src="/img/page000.png" alt="" v-if="i==0"> 
      <div class="info01" v-on:click="info()" v-if="i==0"></div>
      <div class="infobox" v-if="infor && i==0">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">Every year around 500’000 people leave their home countries in Central America. They seek protection from the often extreme violence in their home countries and hope for a better life in the north. However, they are often at the mercy of arbitrariness and violence and repeatedly become the target of criminal gangs. 
          A few months ago, Herenia Gonzalez, a Mexican illustrator, visited a project of Médecins Sans Frontières (MSF) in Mexico City. There she met Gabriela, a Venezuelan girl, who had travelled north with her family. Like many others they had hoped to reach the US.</div>
      </div>
      <img src="/img/page001.png" alt="" v-if="i==1"> 
      <div class="info02" v-on:click="info()" v-if="i==1"></div>
      <img src="/img/page002.png" alt="" v-if="i==2"> 
      <img src="/img/page003.png" alt="" v-if="i==3"> 
      <img src="/img/page004.png" alt="" v-if="i==4"> 
      <div class="info03" v-on:click="info()" v-if="i==4"><img src="../public/img/bird00.png" alt=""></div>
      <div class="infobox" v-if="infor && i==4">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">MSF’s social workers conduct activities with children to help them understand and process their emotions in healthy way. One of the tools our staff use is the “stress-o-meter,” which is like a symbolic thermometer of emotions, showing the level of stress and how to deal with it in the moment.</div>
      </div>
      <img src="/img/page005.png" alt="" v-if="i==5"> 
      <img src="/img/page006.png" alt="" v-if="i==6"> 
      <div class="info03" v-on:click="info()" v-if="i==6"><img src="../public/img/bird00.png" alt=""></div>
      <div class="infobox" v-if="infor && i==6">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">More than 300,000 people tried to cross the Darien Gap in 2024 according to Colombian authorities. This is one of the most dangerous parts of the route, not only because of the rivers but also due to the violence, including sexual violence by local gangs who prey on the vulnerability of the migrants, especially girls and women.</div>
      </div>
      <img src="/img/page007.png" alt="" v-if="i==7"> 
      <img src="/img/page008.png" alt="" v-if="i==8"> 
      <img src="/img/page009.png" alt="" v-if="i==9"> 
      <img src="/img/page010.png" alt="" v-if="i==10"> 
      <div class="info03" v-on:click="info()" v-if="i==10"><img src="../public/img/bird00.png" alt=""></div>
      <div class="infobox" v-if="infor && i==10">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">The journey north is fraught with violence, and exploitation and even kidnapping. In 2024 MSF teams also assisted more than 700 survivors of sexual violence in Mexico and hundreds more in Central America.</div>
      </div>
      <img src="/img/page011.png" alt="" v-if="i==11"> 
      <div class="info03" v-on:click="info()" v-if="i==11"><img src="../public/img/bird00.png" alt=""></div>
      <div class="infobox" v-if="infor && i==11">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">Migrants walk together in human caravans to try to reduce their exposure to violence from the multiple armed actors operating along their journey.</div>
      </div>
      <img src="/img/page012.png" alt="" v-if="i==12"> 
      <div class="info03" v-on:click="info()" v-if="i==12"><img src="../public/img/bird00.png" alt=""></div>
      <div class="infobox" v-if="infor && i==12">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">Our teams support migrants, who have experienced (sexualised) violence and other assaults during their journey, some have even been kidnapped en route. MSF provides activities to help people meet their basic needs and recover from the many hardships. As women on the move are particularly exposed, MSF focuses on women’s health. </div>
      </div>
      <img src="/img/page013.png" alt="" v-if="i==13"> 
      <img src="/img/page014.png" alt="" v-if="i==14"> 
      <img src="/img/page015.png" alt="" v-if="i==15"> 
      <div class="info03" v-on:click="info()" v-if="i==15"><img src="../public/img/bird00.png" alt=""></div>
      <div class="infobox" v-if="infor && i==15">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">The closure of the CBP One app, the online platform for submitting request to enter the country, has left hundreds of people and families like Gabriela’s in limbo. Left without any resources in hostile areas, people are struggling to find new ways to access a safer life, free from violence, harassment and discrimination. </div>
      </div>
    </div>
    <div class="col-1 p-0 my-auto" style="cursor: pointer;">
      <img src="/img/arrow-symbol-arrow-transparent-png-image--34-3464602881.png" alt="" v-if="i<15" v-on:click="nextpage()">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    var that = this;
        return {
          i: 0,
          infor: false
        }
    },
    methods: {
      prevpage() {
      var that = this
      if(that.i > 0){
      that.i -= 1
      that.infor = false
    } },
    nextpage() {
      var that = this
      if(that.i < 15){
      that.i += 1
      that.infor = false

    }
    },
    info(){
      this.infor = true
    },
    disinfo(){
      this.infor = false
    }
}
  }

</script>

<style scoped>
</style>
