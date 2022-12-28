<template>
  <div class="analyze">
      <DescriptionComp/>
  </div>
</template>

<script lang="ts">
import DescriptionComp from "@/components/DescriptionComp.vue";
import {defineComponent} from "vue";

export default defineComponent({
  name: "AnalyzeBox",
  components: {DescriptionComp},
  data() {
    return {
      topic: "Analyze Box"
    }
  }
})
</script>

<style scoped>
.analyze {
  height: 800px;
  width: 400px;
  border: 1px solid black;
  justify-content: flex-end;
}
</style>