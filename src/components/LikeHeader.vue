<template>
  <div>
    <slot>
    <h2>デフォルトタイトル (フォールバックコンテンツ)</h2>
    
    </slot>
    <p>{{headerText}}</p>
  </div>
</template>  

<script>
  export default{
    props: ["headerText"]
  };
</script>

<style>
h1 {
    color:red;
  }
</style>