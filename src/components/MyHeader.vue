<template>
    <div>
        <h1>{{ ProjectTitle }}</h1>
        <br>
        <h4>{{ Country }}</h4>
    </div>
</template>
<script>
export default {
    name: "MyHeader",
    props: {
        ProjectTitle: String,
        Country: String
    }
}
</script>
<style scoped>
div {
    text-align: center;
}
</style>