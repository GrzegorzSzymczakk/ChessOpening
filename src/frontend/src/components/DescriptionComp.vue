<template>
  <div class="description">
    <TextBubbleComp/>
    <WizardComp/>
  </div>
</template>

<script lang="ts">
import WizardComp from "@/components/WizardComp.vue";
import TextBubbleComp from "@/components/TextBubbleComp.vue";
import {defineComponent} from "vue";

export default defineComponent({
  name: "DescriptionComp",
  components: {TextBubbleComp, WizardComp}
})
</script>

<style scoped>
.description{
  height: 200px;
  align-self: flex-end;
  justify-content: flex-end;
  flex-direction: column;
}
</style>