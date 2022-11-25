<template>
  <ChessBoardBox class="container"/>
</template>

<script>
import ChessBoardBox from "@/components/ChessBoardBox";

export default {
  name: 'App',
  components: {ChessBoardBox}
}
</script>

<style>
.container{
  display: grid;
  justify-content: center;
  grid-row-start: 1;
}

</style>
