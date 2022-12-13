<template>
  <div class="analyze">
      <DescriptionComp/>
  </div>
</template>

<script>
import DescriptionComp from "@/components/DescriptionComp";

export default {
  name: "AnalyzeBox",
  components: {DescriptionComp},
  data() {
    return {
      topic: "Analyze Box"
    }
  }
}
</script>

<style scoped>
.analyze {
  height: 800px;
  width: 400px;
  border: 1px solid black;
  justify-content: flex-end;
}
</style>