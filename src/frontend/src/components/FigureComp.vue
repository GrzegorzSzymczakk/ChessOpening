<template>
<div :class="figure==='Pawn' ? 'white-pawn' : ''">

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
}

</style>