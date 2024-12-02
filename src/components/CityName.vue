<template>
    <div class="SiteNames">
        <div v-for="city in city_population" :key="city.id">
            <CityItems :city="city" />
        </div>
    </div>
</template>

<script>
import CityItems from './CityItems.vue'
export default {
    name: 'CityName',
    components: {
        CityItems
    },
    props: {
        city_population: Array
    }
}
</script>


<style scoped>
.SiteNames {
    background-color: rgb(225, 138, 138);
    padding: 1em;
    max-width: 100%;
    height: auto;
    margin-top:30px;
}
</style>
