<template>
  <div v-if="this.isWhite" :draggable="true" class="white" :id="counter">
    <FigureComp :figure="figure" :counter="counter"/>
  </div>
  <div v-else class="black">
    <FigureComp :figure="figure" :counter="counter"/>
  </div>

</template>

<script lang="ts">

import FigureComp from "@/components/FigureComp.vue";
import {defineComponent} from "vue";

export default defineComponent({
  name: "SquareField",
  components: {FigureComp},
  props: ['counter', 'white', 'figure'],
  computed: {
    isWhite() {
      const zeroBasedCounter = this.counter - 1;
      return (zeroBasedCounter % 2 === 1 && zeroBasedCounter % 16 <= 7) || (zeroBasedCounter % 2 === 0 && zeroBasedCounter % 16 >= 8)
    }
  }
})
</script>

<style scoped>

.white {
  background-color: sandybrown;
}

.black {
  background-color: saddlebrown;
}
div{
  justify-content: center;
  align-items: flex-end;
}

</style>