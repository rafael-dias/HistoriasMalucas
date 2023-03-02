<script >
export default {
  data() {
    return {
     
      sequencia:[],
      cartas:[
   { nome:"air", imagem:"./images/air.svg"},
{ nome:"air_24", imagem:"./images/air_24.svg"},
{ nome:"angel_fairy", imagem:"./images/angel_fairy.svg"},
{ nome:"baby", imagem:"./images/baby.svg"},
{ nome:"bag", imagem:"./images/bag.svg"},
{ nome:"bee", imagem:"./images/bee.svg"},
{ nome:"bird", imagem:"./images/bird.svg"},
{ nome:"boat", imagem:"./images/boat.svg"},
{ nome:"book", imagem:"./images/book.svg"},
{ nome:"box", imagem:"./images/box.svg"},
{ nome:"boy", imagem:"./images/boy.svg"},
{ nome:"car", imagem:"./images/car.svg"},
{ nome:"card", imagem:"./images/card.svg"},
{ nome:"cat", imagem:"./images/cat.svg"},
{ nome:"circle", imagem:"./images/circle.svg"},
{ nome:"clock", imagem:"./images/clock.svg"},
{ nome:"cloud", imagem:"./images/cloud.svg"},
{ nome:"clover", imagem:"./images/clover.svg"},
{ nome:"cross", imagem:"./images/cross.svg"},
{ nome:"cup", imagem:"./images/cup.svg"},
{ nome:"dog", imagem:"./images/dog.svg"},
{ nome:"ear", imagem:"./images/ear.svg"},
{ nome:"eye", imagem:"./images/eye.svg"},
{ nome:"fairytale", imagem:"./images/fairytale.svg"},
{ nome:"father_and", imagem:"./images/father_and.svg"},
{ nome:"feather", imagem:"./images/feather.svg"},
{ nome:"fire", imagem:"./images/fire.svg"},
{ nome:"fish", imagem:"./images/fish.svg"},
{ nome:"flower", imagem:"./images/flower.svg"},
{ nome:"footprint", imagem:"./images/footprint.svg"},
{ nome:"forest", imagem:"./images/forest.svg"},
{ nome:"friends", imagem:"./images/friends.svg"},
{ nome:"girl", imagem:"./images/girl.svg"},
{ nome:"glasses", imagem:"./images/glasses.svg"},
{ nome:"hand", imagem:"./images/hand.svg"},
{ nome:"hand_holding", imagem:"./images/hand_holding.svg"},
{ nome:"happy", imagem:"./images/happy.svg"},
{ nome:"heart", imagem:"./images/heart.svg"},
{ nome:"house", imagem:"./images/house.svg"},
{ nome:"idea", imagem:"./images/idea.svg"},
{ nome:"justice", imagem:"./images/justice.svg"},
{ nome:"key", imagem:"./images/key.svg"},
{ nome:"lupe", imagem:"./images/lupe.svg"},
{ nome:"magicwand", imagem:"./images/magicwand.svg"},
{ nome:"map", imagem:"./images/map.svg"},
{ nome:"moon", imagem:"./images/moon.svg"},
{ nome:"mother_son", imagem:"./images/mother_son.svg"},
{ nome:"mountain", imagem:"./images/mountain.svg"},
{ nome:"music", imagem:"./images/music.svg"},
{ nome:"pair", imagem:"./images/pair.svg"},
{ nome:"pet_footprint", imagem:"./images/pet_footprint.svg"},
{ nome:"planet", imagem:"./images/planet.svg"},
{ nome:"question", imagem:"./images/question.svg"},
{ nome:"rainbow_outline", imagem:"./images/rainbow_outline.svg"},
{ nome:"ray", imagem:"./images/ray.svg"},
{ nome:"read", imagem:"./images/read.svg"},
{ nome:"repair_the", imagem:"./images/repair_the.svg"},
{ nome:"ring", imagem:"./images/ring.svg"},
{ nome:"ring_10", imagem:"./images/ring_10.svg"},
{ nome:"road", imagem:"./images/road.svg"},
{ nome:"rope", imagem:"./images/rope.svg"},
{ nome:"sad", imagem:"./images/sad.svg"},
{ nome:"star", imagem:"./images/star.svg"},
{ nome:"sun", imagem:"./images/sun.svg"},
{ nome:"sword", imagem:"./images/sword.svg"},
{ nome:"theater_masks", imagem:"./images/theater_masks.svg"},
{ nome:"tower", imagem:"./images/tower.svg"},
{ nome:"tree", imagem:"./images/tree.svg"},
{ nome:"tresure_chest", imagem:"./images/tresure_chest.svg"},
{ nome:"triangle", imagem:"./images/triangle.svg"},
{ nome:"two_speech", imagem:"./images/two_speech.svg"},
{ nome:"ufo", imagem:"./images/ufo.svg"},
{ nome:"water", imagem:"./images/water.svg"},
{ nome:"witch", imagem:"./images/witch.svg"}
      ]

    }
  },
  methods:{
    Roletar(){
      var de = 0
      var ate = this.cartas.length
      var sequencia = []
      var numa = null
      var limite = 0

      for (let index = 0; index < 5; index++) {
        numa = Math.floor(Math.random() * (ate - de) + de)
        while (sequencia.indexOf(numa) != -1) {
          numa = Math.floor(Math.random() * (ate - de) + de)
        }
        sequencia[index] = numa;
        
      }

      this.sequencia = sequencia

    }
  },
  created() {
    this.Roletar()
  },
  }
</script>

<template>
  <nav class="navbar navbar-dark bg-dark">
  <div class="container-fluid d-flex justify-content-center">
    <img src="/logo.png" alt="" class="img-fluid">
    <!-- <span class="navbar-brand mb-0 h1">Historias Malucas</span> -->
  </div>
</nav>
  <div class="container">
    <br>
    <div class="row justify-content-center">
      <div class="col-sm-4 col-md-2 d-flex justify-content-center" ><img loading="lazy" class="carta img-fluid" :src="cartas[sequencia[0]].imagem"> </div>
      <div class="col-sm-4 col-md-2 d-flex justify-content-center" ><img loading="lazy" class="carta img-fluid" :src="cartas[sequencia[1]].imagem"> </div>
      <div class="col-sm-4 col-md-2 d-flex justify-content-center" ><img loading="lazy" class="carta img-fluid" :src="cartas[sequencia[2]].imagem"> </div>
      <div class="col-sm-4 col-md-2 d-flex justify-content-center" ><img loading="lazy" class="carta img-fluid" :src="cartas[sequencia[3]].imagem"> </div>
      <div class="col-sm-4 col-md-2 d-flex justify-content-center" ><img loading="lazy" class="carta img-fluid" :src="cartas[sequencia[4]].imagem"> </div>
    </div>
    <br>
    <div class="row justify-content-md-center">
      <div class="col-sm-4 col-md-2 d-flex justify-content-center">
        <div class="btn btn-light btn-lg" @click="Roletar()">Roletar</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.carta{
  /* padding: 5px; */
  height: 150px;
  width: 200px;
  background-color: #ffb100;
  margin: 5px;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}


</style>
