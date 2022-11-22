<template>
    <div v-if= "counter % 2 == 0" class="white">{{counter}}</div>
    <div v-else class="brown" >{{counter}}</div>

</template>

<script>

export default {
  name: "SquareField",
  props: ['counter']
}
</script>

<style scoped>

div{
  width: 80px;
  height: 80px;
  border: 1px solid black;
  background-color: red;
}

.white{
  background-color: sandybrown;
}

.brown {
  background-color: saddlebrown;
}
</style>