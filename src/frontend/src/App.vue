<template>
  <div id="app">
    <ChapterBox/>
    <ChessBoardBox class="container"/>
    <AnalyzeBox/>
  </div>
</template>

<script lang="ts">
import ChessBoardBox from '@/components/ChessBoardBox.vue';
import ChapterBox from "@/components/ChapterBox.vue";
import AnalyzeBox from "@/components/AnalyzeBox.vue";

export default {
  name: 'App',
  components: {AnalyzeBox, ChapterBox, ChessBoardBox}
}

</script>

<style>
#app{
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

div {
  display: flex;
}

.container {
  display: grid;
  justify-content: center;
  height: 720px;
  grid-row-start: 1;
}
</style>
