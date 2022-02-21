<template>
  <div class="app">
    <p>
      <JobList :jobs="jobs"/>
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import JobList from "./components/JobsList.vue";
import Job from "./types/Jobs";

export default defineComponent({
  name: "App",
  components: { JobList },
  setup() {
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
