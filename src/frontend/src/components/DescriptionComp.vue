<template>
  <div class="description">
    <TextBubbleComp/>
    <WizardComp/>
  </div>
</template>

<script>
import WizardComp from "@/components/WizardComp";
import TextBubbleComp from "@/components/TextBubbleComp";

export default {
  name: "DescriptionComp",
  components: {TextBubbleComp, WizardComp}
}
</script>

<style scoped>
.description{
  height: 200px;
  align-self: flex-end;
  justify-content: flex-end;
  flex-direction: column;
}
</style>