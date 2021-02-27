<template>
    <h1>Job details Page</h1>
    <div v-if="job">
        <h2>{{ job.title }}</h2>
        <h2>Id: {{ job.id }}</h2>
        <h2>{{ job.details }}</h2>
    </div>
    <div v-else>
        <h1>Content is loading...</h1>
    </div>
</template>

<script>
export default {
    props: ['id'],
    
    data(){
        return{
            job: null
        }
    },
    mounted(){
      fetch('http://localhost:3000/jobs/'+ this.id)
        .then(res => res.json())
        .then(data => this.job = data)
        .catch(err => console.log(err.message))
    }
}
</script>

<style>

</style>