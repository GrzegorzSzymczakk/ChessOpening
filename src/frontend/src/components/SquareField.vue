<template>
    <div v-if="this.isWhite" class="white" :id="counter" >{{counter}}</div>
    <div v-else :id="counter" >{{}}</div>
</template>

<script>

export default {
  name: "SquareField",
  props: ['counter', 'white'],
  computed:{
    isWhite(){
      const zeroBasedCounter = this.counter - 1;
      return (zeroBasedCounter % 2 === 1 && zeroBasedCounter % 16 <= 7) || (zeroBasedCounter % 2 === 0 && zeroBasedCounter % 16 >= 8)
    }
  }
}
</script>

<style scoped>

div{
  width: 80px;
  height: 80px;
  border: 1px solid black;
  background-color: saddlebrown;
}

.white{
  background-color: sandybrown;
}

</style>