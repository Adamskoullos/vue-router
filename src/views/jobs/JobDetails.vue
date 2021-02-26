<template>
    <h1>Job details Page</h1>
    <h2>The current job id is: {{ id }}</h2>
</template>

<script>
export default {
    props: ['id'],
    
    // data(){
    //     return{
    //         id: this.$route.params.id
    //     }
    // }
}
</script>

<style>

</style>