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

<script lang="ts">
import SquareField from "@/components/SquareField.vue";
import {defineComponent} from "vue";

export default defineComponent({
  name: "ChessBoard",
  components: {SquareField},
  data() {
    const whitePawns = [49, 50, 51, 52, 53, 54, 55, 56]
    const blackPawns = [9, 10, 11, 12, 13, 14, 15, 16]
    const whiteBishops = [59, 62]
    const blackBishops = [3, 6]
    const whiteRooks = [57, 64]
    const blackRooks = [1, 8]
    const whiteHorses = [58, 63]
    const blackHorses = [2, 7]


    return {
      whitePawns, blackPawns, whiteBishops, blackBishops, whiteHorses, blackHorses, whiteRooks, blackRooks,
      fieldColor: true,
      whiteQueen: 60,
      whiteKing: 61,
      blackKing: 5,
      blackQueen: 4
    }
  },
  methods: {
    getFigureFor(field:number) {
      switch (true) {
        case field === this.whiteQueen: {
          return "white-queen"
        }
        case field === this.blackQueen: {
          return "black-queen"
        }
        case field === this.whiteKing: {
          return "white-king"
        }
        case field === this.blackKing: {
          return "black-king"
        }
        case this.whitePawns.includes(field): {
          return "white-pawn"
        }
        case this.whiteBishops.includes(field): {
          return "white-bishop"
        }
        case this.whiteHorses.includes(field): {
          return "white-horse"
        }
        case this.whiteRooks.includes(field): {
          return "white-rook"
        }
        case this.blackPawns.includes(field): {
          return "black-pawn"
        }
        case this.blackBishops.includes(field): {
          return "black-bishop"
        }
        case this.blackHorses.includes(field): {
          return "black-horse"
        }
        case this.blackRooks.includes(field): {
          return "black-rook"
        }
        default:
          return ""
      }
    }
  },
  // watch: {
  //   counter() {
  //     this.fieldColor = !this.fieldColor
  //   }
  // }
})
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