<template>
    <div>
        <h1 v-if="display">{{ name }}</h1>
        <button id="header" v-on:click="toggle">Toggle</button>
    </div>
</template>

<script>
    export default {
        name: "Home",
        data() {
            return {
                name: "Init value",
                display: true
            }
        },
        methods: {
            toggle() {
                this.display = !this.display;
            }
        },
        beforeCreate() {
            this.name = "before method"
            console.log(this.name);
        },
        created() {
            this.name = "created method";
            console.log(this.name);
        },
        beforeMount() {
            this.name = "beforeMount method"
            console.log(this.name, this.$el);
        },
        beforeUnmount() {
            console.log("beforeUnmount method", this.$el);
        },
        unmounted() {
            console.log("beforeUnmount method", this.$el);
        },
        mounted() {
            this.name = "mounted method";
            console.log(this.name, this.$el);
        }
    }
</script>

<style scoped>

</style>
