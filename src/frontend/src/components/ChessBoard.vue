<template>
  <p> Hello </p>
  <div class="board">
    <SquareField v-for="field in 64"
                 :key="field"
                 :counter="field"
                 :white="this.fieldColor"
    >
      </SquareField>
  </div>
</template>

<script>
import SquareField from "@/components/SquareField";

export default {
  name: "ChessBoard",
  components: {SquareField},
  data() {
    return {
      fieldColor: true
    }
  },
  watch:{
    counter(){
      this.fieldColor=!this.fieldColor
    }
  }
}
</script>

<style scoped>
.board {
  display: grid;
  grid-template-columns: repeat(8, 80px);
  grid-template-rows: repeat(8, 80px);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 640px;
  height: 640px;
  border: 1px solid black;
}
</style>