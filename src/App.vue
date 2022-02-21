<template>
  <div class="app">
    <p>
      {{ jobs[0].location }}
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import Job from "./types/Jobs";

export default defineComponent({
  name: "App",
  components: {},
  setup() {
    // const state = reactive({
    //   name: "Link",
    //   age: 25 as string | number,
    // });
    // state.name = 999; // cannot change type
    // state.age = "26";
    // return { ...toRefs(state) };
    // const name = ref("Link");
    // const age = ref<number | string>(25);
    // return { name, age };
    const jobs = ref<Job[]>([
      { title: "farm workes", location: "lala land", salary: 30000, id: "1" },
      {
        title: "quarry man",
        location: "death mountain",
        salary: 35000,
        id: "2",
      },
      {
        title: "flute player",
        location: "the lost woods",
        salary: 400000,
        id: "3",
      },
      { title: "fisherman", location: "lake hylia", salary: 21000, id: "4" },
      {
        title: "prison guard",
        location: "gerudo valley",
        salary: 50000,
        id: "5",
      },
    ]);

    return { jobs };
  },
});
</script>

<style>
</style>
