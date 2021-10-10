<template>
    <div>
        <h1>{{ name }}</h1>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
        name: "Home",
        data() {
            return {
                name: "Init value",
                display: true
            }
        },
        mounted() {
            axios.get('https://dummy.restapiexample.com/api/v1/employees')
                .then((resp) => console.log(resp));
        }
    }
</script>

<style scoped>

</style>
