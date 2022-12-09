<template>
    <div v-if="this.isWhite" class="white" :id="counter" >
      {{counter}}
      <FigureComp :figure="figure"/>
    </div>
    <div v-else>{{counter}}</div>
</template>

<script>

import FigureComp from "@/components/FigureComp";
export default {
  name: "SquareField",
  components: {FigureComp},
  props: ['counter', 'white', 'figure'],
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