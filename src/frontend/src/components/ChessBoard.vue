<template>
  <div class="board">
    <SquareField v-for="field in 64"
                 :key="field"
                 :counter="field"
                 :white="this.fieldColor"
                 :figure="this.getFigureFor(field)">
    </SquareField>
  </div>
</template>

<script>
import SquareField from "@/components/SquareField";

export default {
  name: "ChessBoard",
  components: {SquareField},
  data() {
    const whitePawns = [3, 5, 6, 13]
    return {
      whitePawns,
      fieldColor: true,
      whiteQueen: 60
    }
  },
  methods: {
    getFigureFor(field) {
      switch (true) {
        case field === this.whiteQueen: {
          console.log("wh_queen")
          return "white-queen"
        }
        case field === 30: {
          console.log("blqu")
          return "black-queen"
        }
        case this.whitePawns.includes(field): {
          console.log("wh_pawn")
          return "white-pawn"
        }
        default:
          console.log("dupass")
          return null
      }
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

</style>