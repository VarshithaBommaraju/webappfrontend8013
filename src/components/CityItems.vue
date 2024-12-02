<template>
    <div>
        <h2>{{ city.city }}</h2>
        <h4>Female Population: {{ city.female_population }} </h4>
        <h4>Male Populaiton: {{ city.male_population }}</h4>
        <h4>Count of Minors: {{ city.minors_count }}</h4>
        <h4>Count of Adults: {{ city.adult_count }}</h4>
        <h4>Population Density Index: {{ city.density_index }}</h4>
    </div>
</template>

<script>
export default {
    name: 'CityItems',
    props: {
        city: Array
    }
}
</script>

<style scoped>
h1 {
    border: 3px solid black;
    background-color: rgb(221, 242, 242);
}
h2{
    text-align: center;
}
div {
    text-align: center;
    background-color: white;
    color: black;
    padding: 1em;
    margin: 5px;
    font-weight: bold;
    font-size: 15px;
}
</style>
