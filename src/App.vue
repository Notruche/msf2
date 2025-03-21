<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="row p-0 m-0 page">
    <div class="col-1 p-0 my-auto" style="cursor: pointer;">
      <img src="/img/left-arrow-png-file-2608997235.png" alt="" v-if="i>0" v-on:click="prevpage()">
    </div>
    <div class="col-10 p-0 my-auto grille"> 
      <div class="infobox" v-if="refresh">
        <div class="x" v-on:click="noredo()">X</div>
        <div class="infotext row"><p class="col-12">Go back to the first page ?</p> <br>
          <div class="col-2"></div>
          <div class="btn btn-success col-2" v-on:click="goback()">Yes</div>
          <div class="col-4"></div>
          <div class="btn btn-danger col-2" v-on:click="noredo()">No</div>
          <div class="col-2"></div>
        </div>
      </div>
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
      <div class="info03" v-on:click="info()" v-if="i==4"><img src="/img/bird00.png" alt=""></div>
      <div class="info04" v-on:click="info2()" v-if="i==4"><img src="/img/doll01.png" alt=""></div>
      <div class="infobox" v-if="infor && i==4">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">MSF’s social workers conduct activities with children to help them understand and process their emotions in healthy way. One of the tools our staff use is the “stress-o-meter,” which is like a symbolic thermometer of emotions, showing the level of stress and how to deal with it in the moment.</div>
      </div>
      <div class="infobox" v-if="infor2 && i==4">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">MSF psychological teams use Quitapenas in some situations to provide mental health care for patients in Mexico. These small, handmade "worry dolls" are originally  from Guatemala. According to the legend, when worrying keeps a person awake, he or she tells a worry to as many dolls as necessary before placing them under the pillow. The dolls take over the worrying for the person who then sleeps peacefully through the night. Even though these dolls offer comfort and support, they are no substitute for professional therapy.</div>
      </div>
      <img src="/img/page005.png" alt="" v-if="i==5"> 
      <img src="/img/map00.png" alt="" v-if="i==6">
      <div class="info05" v-on:click="info()" v-if="i==6"><img src="/img/bird06.png" alt=""></div>
      <img src="/img/page006.png" alt="" v-if="i==7"> 
      <div class="info03" v-on:click="info()" v-if="i==7"><img src="/img/bird01.png" alt=""></div>
      <div class="infobox" v-if="infor && i==7">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">More than 300,000 people tried to cross the Darien Gap in 2024 according to Colombian authorities. This is one of the most dangerous parts of the route, not only because of the rivers but also due to the violence, including sexual violence by local gangs who prey on the vulnerability of the migrants, especially girls and women.</div>
      </div>
      <img src="/img/map00.png" alt="" v-if="i==8">
      <div class="info06" v-on:click="info()" v-if="i==8"><img src="/img/bird06.png" alt=""></div>
      <img src="/img/page007.png" alt="" v-if="i==9"> 
      <img src="/img/page008.png" alt="" v-if="i==10"> 
      <img src="/img/page009.png" alt="" v-if="i==11"> 
      <img src="/img/map00.png" alt="" v-if="i==12">
      <div class="info07" v-on:click="info()" v-if="i==12"><img src="/img/bird06.png" alt=""></div>
      <img src="/img/page010.png" alt="" v-if="i==13"> 
      <div class="info03" v-on:click="info()" v-if="i==13"><img src="../public/img/bird02.png" alt=""></div>
      <div class="infobox" v-if="infor && i==13">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">The journey north is fraught with violence, and exploitation and even kidnapping. In 2024 MSF teams also assisted more than 700 survivors of sexual violence in Mexico and hundreds more in Central America.</div>
      </div>
      <img src="/img/page011.png" alt="" v-if="i==14"> 
      <div class="info03" v-on:click="info()" v-if="i==14"><img src="../public/img/bird03.png" alt=""></div>
      <div class="infobox" v-if="infor && i==14">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">Migrants walk together in human caravans to try to reduce their exposure to violence from the multiple armed actors operating along their journey.</div>
      </div>
      <img src="/img/page012.png" alt="" v-if="i==15"> 
      <div class="info03" v-on:click="info()" v-if="i==15"><img src="../public/img/bird04.png" alt=""></div>
      <div class="infobox" v-if="infor && i==15">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">Our teams support migrants, who have experienced (sexualised) violence and other assaults during their journey, some have even been kidnapped en route. MSF provides activities to help people meet their basic needs and recover from the many hardships. As women on the move are particularly exposed, MSF focuses on women’s health. </div>
      </div>
      <img src="/img/page013.png" alt="" v-if="i==16"> 
      <img src="/img/page014.png" alt="" v-if="i==17"> 
      <img src="/img/page015.png" alt="" v-if="i==18"> 
      <div class="info03" v-on:click="info()" v-if="i==18"><img src="../public/img/bird05.png" alt=""></div>
      <div class="infobox" v-if="infor && i==18">
        <div class="x" v-on:click="disinfo()">X</div>
        <div class="infotext">The closure of the CBP One app, the online platform for submitting request to enter the country, has left hundreds of people and families like Gabriela’s in limbo. Left without any resources in hostile areas, people are struggling to find new ways to access a safer life, free from violence, harassment and discrimination. </div>
      </div>
      <div class="formulaire row" v-if="i==19">
        <div class="col-12">Rate this comic ! </div>
        <img style= "cursor:pointer" v-on:click="rate1()" v-on:mouseover="starhover1()" v-on:mouseleave="starleave()" class="col-1" :src=star1 alt="">
        <img style= "cursor:pointer" v-on:click="rate2()" v-on:mouseover="starhover2()" v-on:mouseleave="starleave()" class="col-1" :src=star2 alt="">
        <img style= "cursor:pointer" v-on:click="rate3()" v-on:mouseover="starhover3()" v-on:mouseleave="starleave()" class="col-1" :src=star3 alt="">
        <img style= "cursor:pointer" v-on:click="rate4()" v-on:mouseover="starhover4()" v-on:mouseleave="starleave()" class="col-1" :src=star4 alt="">
        <img style= "cursor:pointer" v-on:click="rate5()" v-on:mouseover="starhover5()" v-on:mouseleave="starleave()" class="col-1" :src=star5 alt="">
        <form
                      action=""
                      target="blank"
                      method="POST"
                      class="col-10 row d-flex container-fluid justify-content-center"
                    >

                      <textarea
                        name="Message"
                        class="col-12 mt-3 mb-3"
                        id="Message"
                        v-model="message"
                      ></textarea>

                      <input
                        type="submit"
                        value="Envoyer"
                        class="col-4 mb-3 download mr-1"
                        v-if="nom!=='' && email!=='' && message!==''"
                      >
                      <input type="reset" value="Reset" class="col-4 mb-3 download ml-1">
                    </form>
      </div>
    </div>
    <div class="col-1 p-0 right">
      <img src="/img/arrow-symbol-arrow-transparent-png-image--34-3464602881.png" alt="" class="arrowR" v-if="i<19" v-on:click="nextpage()" style="cursor: pointer;">
      <img src="/img/refresh.png" alt="" class="returnTo" v-on:click="redo()" style="cursor: pointer;">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    var that = this;
        return {
          i: 0,
          infor: false,
          infor2: false,
          refresh: false,
          star1: "/msf2/img/star-empty.png",
          star2: "/msf2/img/star-empty.png",
          star3: "/msf2/img/star-empty.png",
          star4: "/msf2/img/star-empty.png",
          star5: "/msf2/img/star-empty.png",
          lockrating: false
          // idletime: 0,
          // idlewarn(){that.refresh = true},
        }
    },
    methods: {
      // idle(){
      // var that = this
      // clearTimeout(that.idletime)
      // if(that.i > 0){
     // that.idletime = setTimeout(function(){
        //that.idlewarn()
        //  },300000)
       // }
   // },
      prevpage() {
      var that = this
      if(that.i > 0){
      that.i -= 1
      that.infor = false
      that.infor2 = false
      that.refresh = false
    } },
    nextpage() {
      var that = this
      if(that.i < 19){
      that.i += 1
      that.infor = false
      that.infor2 = false
      that.refresh = false

    }
    },
    info(){
      this.infor = true
    },
    info2(){
      this.infor2 = true
    },
    disinfo(){
      this.infor = false
      this.infor2 = false
    },
    redo(){
      this.refresh = true
    },
    noredo(){
      this.refresh = false
    },
    goback(){
      this.i=0
      this.refresh = false
    },
    starhover1(){
      if(this.lockrating == false) {
      this.star1 = "/msf2/img/star-full.png"}
    },
    starhover2(){
      if(this.lockrating == false) {
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"}
    },
    starhover3(){
      if(this.lockrating == false) {
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-full.png"}
    },
    starhover4(){
      if(this.lockrating == false) {
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-full.png"
      this.star4 = "/msf2/img/star-full.png"}
    },
    starhover5(){
      if(this.lockrating == false) {
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-full.png"
      this.star4 = "/msf2/img/star-full.png"
      this.star5 = "/msf2/img/star-full.png"}
    },
    starleave(){
      if(this.lockrating == false) {
      this.star1 = "/msf2/img/star-empty.png"
      this.star2 = "/msf2/img/star-empty.png"
      this.star3 = "/msf2/img/star-empty.png"
      this.star4 = "/msf2/img/star-empty.png"
      this.star5 = "/msf2/img/star-empty.png"}
    },
    rate1(){
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-empty.png"
      this.star3 = "/msf2/img/star-empty.png"
      this.star4 = "/msf2/img/star-empty.png"
      this.star5 = "/msf2/img/star-empty.png"
      this.lockrating = true
    },
    rate2(){
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-empty.png"
      this.star4 = "/msf2/img/star-empty.png"
      this.star5 = "/msf2/img/star-empty.png"
      this.lockrating = true
    },
    rate3(){
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-full.png"
      this.star4 = "/msf2/img/star-empty.png"
      this.star5 = "/msf2/img/star-empty.png"
      this.lockrating = true
    },
    rate4(){
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-full.png"
      this.star4 = "/msf2/img/star-full.png"
      this.star5 = "/msf2/img/star-empty.png"
      this.lockrating = true
    },
    rate5(){
      this.star1 = "/msf2/img/star-full.png"
      this.star2 = "/msf2/img/star-full.png"
      this.star3 = "/msf2/img/star-full.png"
      this.star4 = "/msf2/img/star-full.png"
      this.star5 = "/msf2/img/star-full.png"
      this.lockrating = true
    },
}
  }

</script>

<style scoped>
</style>
