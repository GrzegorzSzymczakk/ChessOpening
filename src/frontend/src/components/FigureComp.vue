<template>
  <img v-if="figure!==''"
       :draggable="true"
       :src="getUrl() + figure + '.png)'"
  />
<!--        :src="`${process.env.BASE_URL}white_horse.png`"-->
<!--       ondragstart="console.log('hej')"-->
  <!--       :src="'src/assets/' + figure + '.png'"-->
  <div v-else
       draggable="true"
       class="no-figure"
       ondragstart="console.log('hej')"
  >
    {{ counter }}
  </div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({
  name: "FigureComp",
  props: ['figure', 'counter'],
  methods: {
    getUrl() {
      return '@/assets/'
    }
  }
})
</script>

<style scoped>

.white-pawn{
  content: url("../assets/white_pawn.png");
}

.black-pawn {
  content: url("../assets/white_pawn.png");
  filter: invert(100%);
}

.black-queen {
  content: url("../assets/black_queen.png");
}

.white-queen {
  content: url("../assets/white_queen.png");
}

.black-king {
  content: url("../assets/black_king.png");
}

.white-king {
  content: url("../assets/white_king.png");
}

.white-bishop {
  content: url("../assets/white_bishop.png");
}

.black-bishop {
  content: url("../assets/black_bishop.png");
}

.white-horse {
  content: url("../../public/white_horse.png");
}

.black-horse {
  content: url("../../public/white_horse.png");
  filter: invert(90%);
}

.white-rook {
  content: url("../assets/white_rook.png");
  max-width: 100%;
}

.black-rook {
  content: url("../assets/black-rook.png");
  max-width: 100%;
}

div {
  max-width: 100%;
  max-height: 75px;
}
img {
  max-width: 100%;
  max-height: 75px;
}

</style>