<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h2>{{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          title: "Ninja UX Designer",
          id: 1,
          details:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis, iusto?",
        },
        {
          title: "Ninja Web Developer",
          id: 2,
          details:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Neque molestias consequuntur dignissimos obcaecati! Labore.",
        },
        {
          title: "Ninja Vue Developer",
          id: 3,
          details:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nemo.",
        },
      ],
    };
  },
};
</script>

<style>
.job h2 {
  background: #f4f4f4;
  padding: 20px;
  border: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h2:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
