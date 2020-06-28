<template>
  <v-app>
    <v-card
      class="align-center justify-center pa-4 mx-auto my-5"
      max-width="550"
      min-height="76"
      outlined
    >
      <div class="font-weight-bold">
        あなたはこのゲームに参加しますか？
      </div>
      <ul>
        <li>コイントス、表が出たら1万円払わなければならない</li>
        <li>コイントス、裏が出たら1万円もらえる</li>
      </ul>
    </v-card>
    <div class="d-flex mx-auto">
      <div class="my-2 mr-5">
        <v-btn @click="cointoss" x-large width="200px" color="success" dark>参加する</v-btn>
      </div>
      <div class="my-2">
        <v-btn x-large width="200px" color="error" dark>参加しない</v-btn>
      </div>
    </div>
    <div class="mx-auto my-2" v-show="flag">
      コイントスの結果 
      <span class="font-weight-bold red--text text--lighten-1"> {{ this.sides }} </span>
      でした
    </div>
    <h3
      class="mx-auto"
    >現在の残金は {{ price }} 円です</h3>
    <!-- <v-content>
      <LossDodgeLaw/>
    </v-content> -->
  </v-app>
</template>

<script>
// import LossDodgeLaw from './components/LossDodgeLaw';

export default {
  name: 'App',

  // components: {
  //   LossDodgeLaw,
  // },

  data: () => ({
    price: 0,
    goal: 100000,
    flag: false,
    sides: "表"
  }),
  methods: {
    cointoss: function () {
      let side = Math.floor(Math.random() * Math.floor(2))

      this.price += side ? 10000 : -10000
      this.flag = true
      this.sides = side ? "表" : "裏" 
    }
  }
};
</script>
