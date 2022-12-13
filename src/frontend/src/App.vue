<template>
  <ChapterBox/>
  <ChessBoardBox class="container"/>
  <AnalyzeBox/>
</template>

<script>
import ChessBoardBox from "@/components/ChessBoardBox";
import ChapterBox from "@/components/ChapterBox";
import AnalyzeBox from "@/components/AnalyzeBox";

export default {
  name: 'App',
  components: {AnalyzeBox, ChapterBox, ChessBoardBox}
}
</script>

<style>
div{
  display: flex;
}
.container{
  display: grid;
  justify-content: center;
  height: 720px;
  grid-row-start: 1;
}
</style>
