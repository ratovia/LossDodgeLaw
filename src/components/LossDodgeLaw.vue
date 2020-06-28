<template>
  <!-- <v-question-section 
    class=" mx-auto"
    width="100vw"
  >
    <h1>あなたはこのゲームに参加しますか？</h1>
    <ul>
      <li>表が出たら一万円払わなければならない</li>
      <li>裏が出たら二万円もらえる</li>
    </ul>
    <div class="buttons d-flex">
      <button>参加する</button>
      <button>参加しない</button>
    </div>
    <h3>あなたの残金 {{ price }} 円</h3>
  </div> -->
  <v-card
    class="align-center justify-center pa-4 mx-auto my-5"
    max-width="550"
    min-height="76"
    outlined
  >
    <div :class="`text-${model}`">
      あなたはこのゲームに参加しますか？
    </div>
    <ul>
      <li>表が出たら一万円払わなければならない</li>
      <li>裏が出たら二万円もらえる</li>
    </ul>
  </v-card>
</template>

<script>
export default {
  data: function (){
    return {
      price: 0,
      goal: 100000
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
