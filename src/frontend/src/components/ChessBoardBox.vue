<template>
  <div class="flex-box">
    <ChessBoard class="centre"/>
    <CoordinateNumbers class="right"/>
    <CoordinateLetters class="bottom"/>
  </div>
</template>

<script lang="ts">
import ChessBoard from "@/components/ChessBoard.vue";
import CoordinateNumbers from "@/components/labeling/CoordinateNumbers.vue";
import CoordinateLetters from "@/components/labeling/CoordinateLetters.vue";
import {defineComponent} from "vue";

export default defineComponent({
  name: "ChessBoardBox",
  components: {ChessBoard, CoordinateNumbers, CoordinateLetters}
})
</script>

<style scoped>
.centre{

}
.right {
  display: grid;
  width: 80px;
  height: 640px;
  grid-column-start: 2;
}
.bottom{
  grid-row-start: 2;
}

</style>