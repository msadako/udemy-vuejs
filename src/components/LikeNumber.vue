<template>
<div>
  <p>いいね({{ halfNumber }})</p>
  <p>{{totalNumber /2}}</p>
  <button @click="increment">+1</button>
</div>
</template>

<script>

export default{
  //props:["totalNumber","testProps"],
  props:{
    totalNumber: {
      type: Number,
      required: true,
      default :10
    },
    testProps: {
      type: String
    }
  },
  computed:{
    halfNumber(){
      return this.totalNumber / 2
    }
  },
  methods: {
    increment(){
      //this.number += 1;
      this.$emit("my-click", this.totalNumber + 1);
    }
  }
}

</script>

<style scoped>
  div{
    border:1px solid red;
  }
</style>