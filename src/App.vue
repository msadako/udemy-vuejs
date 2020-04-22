<template>
  <div>

    <like-header header-text="ハロー">
      <h1>トータルのいいね数</h1>
      <h2>{{number}}</h2>
    </like-header>
    
    <LikeNumber v-bind:totalNumber="number" v-on:my-click="number = $event"></LikeNumber>
    <LikeNumber v-bind:total-number="number"></LikeNumber>
  </div>
</template>

<script>

//ローカル登録
import LikeHeader from "./components/LikeHeader.vue";

export default{
  data(){
    return {number:10};
  },
  components: {
    LikeHeader: LikeHeader
    //短縮可能 LikeHeader
  }
}

</script>


<style scoped>
  div{
    border:1px solid blue;
  }
  h1 {
    color:blue;
  }
</style>
