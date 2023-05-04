<template>
    <div class="single-president">
        <h2>{{ president.id }} president</h2><hr>
        <h2 class="president-info">{{ president.Name }}</h2><hr>
        <p class="president-info"><br><b>Ruling Year:</b> {{ president.Ryear }}</p>
        <p class="president-info"><b>Date of Birth: </b>{{ president.dob }}</p>
        <p class="president-info"><b>President at the age of: </b>{{ president.pyear }}</p>
        <p class="president-info"><b>Degree:</b> {{ president.degree }}</p>
        <a :href="president.reference" target="_blank" class="president-link">Reference</a>

    </div>
</template>

<script>

export default {
    name: 'SPresident',
    props: {
        president: Array
    }
}
</script>

<style scoped>
h2 {
    margin: 2px;
    font-family: monospace;
    font-size: 23px;
}

.single-president {
    background-color: rgba(137, 195, 243, 0.2);;
    font-family: Georgia, 'Times New Roman', Times, serif;
    color: black;
    padding: 1em;
    text-align: center;
    width: 400px;
    border-radius: 5px;
    margin: 10px;
}

.president-info {
    margin: 5px 0;
}

.president-link {
    display: block;
    margin-top: 10px;
    color: #0057ff;
    text-decoration: none;
}

.president-link:hover {
    text-decoration: underline;
}
</style>