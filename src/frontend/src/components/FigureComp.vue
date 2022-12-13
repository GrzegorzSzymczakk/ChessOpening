<template>
  <div v-if="figure!==''" :class="figure"></div>
  <div v-else >{{counter}}</div>
</template>

<script>
export default {
  name: "FigureComp",
  props: ['figure','counter']
}
</script>

<style scoped>

.white-pawn {
  content: url("../assets/white_pawn.png");
}
.black-pawn {
  content: url("../assets/white_pawn.png");
  filter: invert(100%);
}

.black-queen {
  content: url("../assets/black_queen.png");
}

.white-queen {
  content: url("../assets/white_queen.png");
}
.black-king {
  content: url("../assets/black_king.png");
}
.white-king {
  content: url("../assets/white_king.png");
}
.white-bishop {
  content: url("../assets/white_bishop.png");
}
.black-bishop {
  content: url("../assets/black_bishop.png");
}
.white-horse {
  content: url("../assets/white_horse.png");
}
.black-horse {
  content: url("../assets/white_horse.png");
  filter: invert(90%);
}
.white-rook {
  content: url("../assets/white_rook.png");
  max-width: 100%;
}
.black-rook {
  content: url("../assets/black_rook.png");
  max-width: 100%;
}
div{
  max-width: 100%;
  max-height: 75px;
}

</style>