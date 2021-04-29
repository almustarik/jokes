<template>
    <form @submit.prevent="obSubmit">
        <input type="text" v-model="text" placeholder="Search Jokes..">
        <input type="submit" value="Search Jokes">
    </form>
</template>

<script>
export default {
    name: "SearchJokes",
    data() {
        return {
            text: "",
        };
    },
    methods: {
        obSubmit() {
            this.$emit("search-text", this.text);
            this.text = "";
        }
    }
}
</script>

<style>

</style>