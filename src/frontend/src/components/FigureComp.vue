<template>
<!--<div id="test" :class="figure==='Pawn' ? 'white-pawn' : ''">-->
<div id="test" :class="figure">

</div>

</template>

<script>
export default {
  name: "FigureComp",
  props:['figure']
}
</script>

<style scoped>
.white-pawn{
  content: url("../assets/white_pawn.png");
  background-color: transparent;
}
.black-queen{
  content: url("../assets/black_queen.png");
  background-color: transparent;
}
.white-queen{
  content: url("../assets/white_queen.png");
  background-color: transparent;
}


</style>