<template>
  <div class="board">
    <SquareField v-for="field in 64"
                 :key="field"
                 :counter="field"
                 :white="this.fieldColor"
                 :figure="this.getFigureFor(field)">
    </SquareField>
  </div>
<!--  <SquareField class="img"></SquareField>-->
</template>

<script>
import SquareField from "@/components/SquareField";

export default {
  name: "ChessBoard",
  components: {SquareField},
  data() {
    const whiteFigures = [3,5,6,13]
    return {
      whiteFigures,
      fieldColor: true
    }
  },
  methods: {
    getFigureFor(field){
      if(this.whiteFigures.includes(field)){
        console.log(field)
        return "Pawn"
      }
      return null
    }
  },
  watch: {
    counter() {
      this.fieldColor = !this.fieldColor
    }
  }
}
</script>

<style scoped>
.board {
  display: grid;
  grid-template-columns: repeat(8, 80px);
  grid-template-rows: repeat(8, 80px);
  width: 640px;
  height: 640px;
  border: 1px solid black;
}
.img{
  content: url("../assets/white_pawn.png");
}

</style>