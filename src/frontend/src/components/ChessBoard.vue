<template>
  <p> Hello</p>
  <div class="board">
    <SquareField v-for="field in 64" :key="field">
    </SquareField>
  </div>
</template>

<script>

import SquareField from "@/components/SquareField";
export default {
  name: "ChessBoard",
  components: {SquareField},
  data() {
    const fields = [0,0,0,3,3,3,3,3,3,3,3]
    return{
      fields
    }
  },
  methods: {
    testAlarm(){
      alert("Hello")
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

.square {
  height: 80px;
  width: 80px;
  border: 1px solid black;
}

.black {
  background: black;
}

.white {
  background: sandybrown;
}


</style>