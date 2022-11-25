<template>
<div class="analyze">
  <h2>{{topic}}</h2>

</div>
</template>

<script>
export default {
  name: "AnalyzeBox",
  data(){
    return{
      topic: "Analyze Box"
    }
  }
}
</script>

<style scoped>
.analyze{
  height: 500px;
  width: 250px;
  border: 1px solid black;
}

</style>