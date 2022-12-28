<template>
  <div class="bubble">Hei, i am teacher, and here in the text cloud i ll give you some hints about next move!</div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({
  name: "TextBubbleComp"
})
</script>

<style scoped>
.bubble {
  margin: 10px 12px 6px;
  padding: 4px 8px 8px;
  box-shadow: 0 1px 6px rgba(0, 0, 0, 0.3), inset 0 -4px 0 rgba(0, 0, 0, 0.12);
  background: #F7D93B;
  border-radius: 8px;
  max-width: 240px;
  min-width: 150px;
  text-shadow: 0 2px rgba(0, 0, 0, 0.12);
}

</style>