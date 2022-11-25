<template>
  <div>
    <label class="letters" v-for="letter in letters" :key="letter">
      {{letter.val}}
    </label>
  </div>
</template>

<script>
export default {
  name: "CoordinateLetters",
  data() {
    return {
      letters: [
        {val:'A'},{val:'B'},
        {val:'C'},{val:'D'},
        {val:'E'},{val:'F'},
        {val:'G'},{val:'H'},
      ]
    }
  }
}
</script>

<style scoped>
div {
  display: grid;
  width: 640px;
  height: 80px;
  grid-template-columns: repeat(8, 80px);
}
.letters{
  padding: 10px;
  text-align: center;
}

</style>