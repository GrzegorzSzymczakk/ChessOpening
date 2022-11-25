<template>
  <div>
    <label class="numbers" v-for="num in 8" :key="num">
      {{9-num}}
    </label>
  </div>
</template>

<script>
export default {
  name: "CoordinateNumbers"
}
</script>

<style scoped>
div {
  display: grid;
  width: 640px;
  height: 80px;
  grid-template-rows: repeat(8, 80px);
}
.numbers{
  padding: 20px;
  position: relative;
  top: 10%;
}

</style>