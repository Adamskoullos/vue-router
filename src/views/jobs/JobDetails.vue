<template>
    <h1>Job details Page</h1>
    <h2>Title: {{ job.title }}</h2>
    <h2>Id: {{ job.id }}</h2>
    <h2>Details: {{ job.details }}</h2>
</template>

<script>
export default {
    props: ['id'],
    
    data(){
        return{
            job: []
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