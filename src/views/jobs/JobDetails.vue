<template>
  <h1>Job details page</h1>
  <div v-if="job">
  <p>{{job.title}}</p>
  <p>The job id is {{ id }} </p> <!-- see App.vue -->
  <p>{{job.details}} </p> <!-- see App.vue -->
  </div>
  <div v-else>
      <p>Loading...</p>
  </div>
</template>

<script>

export default {
  props: ['id'],
  data(){
    return {
        job: null
    }
  },
  mounted(){
      fetch('http://localhost:3000/jobs/' + this.id)
      .then(res => res.json())
      .then(data => this.job = data)
      .catch(err => console.log(err.message))
  }
}
</script>

<style>
</style>