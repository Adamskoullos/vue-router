<template>
  <h1>UX Design Jobs:</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
      <router-link :to="{ name: 'JobDetails', params: {id: job.id} }">
          <h2>{{ job.title }}</h2>
      </router-link>
  </div>
</template>

<script>
export default {
    data(){
        return{
            jobs:[
                {title:'User Stories', id: 1, details: 'Profile users and create user experience stories'},
                {title:'Content layout', id: 2, details: 'Create wireframes for the content in each view'},
                {title:'Interaction Design', id: 3, details: 'Identify User interaction and interactive feedback'},
                {title:'Functional Design', id: 4, details: 'Identify and map workflows and create logic flow'}
                
            ]
        }
    }
}
</script>

<style>
.job h2{
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #444;
  }
  .job h2:hover {
    background: #ddd;
  }
  .job a{
    text-decoration: none;
  }
</style>