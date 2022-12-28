<template>
  <div class="wizard"></div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({
  name: "WizardComp"
})
</script>

<style scoped>

.wizard {
  content: url("../assets/wizard.png");
  max-width: 20%;
  align-self: flex-end;
}
</style>