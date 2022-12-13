<template>
  <div class="description">
    <WizardComp/>
  </div>
</template>

<script>
import WizardComp from "@/components/WizardComp";

export default {
  name: "DescriptionComp",
  components: {WizardComp}
}
</script>

<style scoped>
.description{
  height: 200px;
  align-self: flex-end;
  justify-content: flex-end;
}
</style>