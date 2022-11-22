<template>
  <div class="flex-box">
    <ChessBoard class="centre"/>
    <CoordinateNumbers class="right"/>
    <CoordinateLetters class="bottom"/>
  </div>
</template>

<script>
import ChessBoard from "@/components/ChessBoard";
import CoordinateNumbers from "@/components/labeling/CoordinateNumbers";
import CoordinateLetters from "@/components/labeling/CoordinateLetters";

export default {
  name: "ChessBoardBox",
  components: {ChessBoard, CoordinateNumbers, CoordinateLetters}
}
</script>

<style scoped>
.centre{

}
.right {
  display: flex;
  width: 80px;
  height: 640px;
  border: 1px solid black;
  grid-column-start: 2;
}
.bottom{
  grid-row-start: 2;
}

</style>