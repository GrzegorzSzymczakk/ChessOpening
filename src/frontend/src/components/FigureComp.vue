<template>
  <div v v-if="figure!=''" :class="figure"></div>
  <div v-else >{{counter}}</div>
</template>

<script>
export default {
  name: "FigureComp",
  props: ['figure','counter']
}
</script>

<style>

.white-pawn {
  content: url("../assets/white_pawn.png");
  background-color: transparent;
}

.black-queen {
  content: url("../assets/black_queen.png");
  background-color: transparent;
  max-width: 100%;
}

.white-queen {
  content: url("../assets/white_queen.png");
  background-color: transparent;
  max-width: 100%;
}
.white-bishop {
  content: url("../assets/white_bishop.png");
  /*background-color: transparent;*/
  max-width: 100%;
  filter: invert(48%) sepia(13%) saturate(3207%) hue-rotate(130deg) brightness(95%) contrast(80%);

}



</style>