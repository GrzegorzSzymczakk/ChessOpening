<template>
  <div class="chapter">
    <select class="course" v-model="pattern">
      <option v-for="course in courses" :key="course">{{ course }}</option>
    </select>
    <nav class="chapters">
      <ul v-for="chapter in filteredByCourse"
          :key="chapter.cat">
        <li>
          {{ chapter.name }}
        </li>

      </ul>
    </nav>
  </div>
</template>

<script lang="ts">
import {defineComponent} from "vue";

type Chapter = {
  name: string;
  cat: string;
}
export default defineComponent({
  name: "ChapterBox",
  data() {
    const chapters: Chapter[] = [
      {
        name: 'Rubinstein',
        cat: 'French Defense'
      },
      {
        name: 'Dragon',
        cat: 'Sicilian Defense'
      },
      {
        name: 'Dragon1',
        cat: 'Sicilian Defense'
      },
      {
        name: 'Dragon2',
        cat: 'Sicilian Defense'
      },
      {
        name: 'Dragon3',
        cat: 'Sicilian Defense'
      },
      {
        name: 'Dragon4',
        cat: 'Sicilian Defense'
      },
      {
        name: 'Dragon5',
        cat: 'Sicilian Defense'
      }
    ];

    return {
      pattern: "",
      courses: ['French Defense', 'Ruy Lopez', 'Sicilian Defense'],
      chapters
    }
  },
  computed: {
    filteredByCourse(): Chapter[] {
      let filter = new RegExp(this.pattern, 'i');
      return this.chapters.filter(el => el.cat.match(filter))
    }
  }
})
</script>
<style scoped>

.chapter {
  height: 250px;
  width: 300px;
  border: 1px solid black;
  display: flex;
  flex-direction: column;
}

.course {
  width: 200px;
  height: 40px;
}

.chapters {
  overflow-y: scroll;
}
</style>