<template>
  <div class="container">
    <div class="inside-container">
      <HeaderTop TopicName="City Population Explorer In USA" />
    <CityName :city_population="city_population" />
    </div>
    
  </div>
</template>

<script>
import HeaderTop from './components/HeaderTop.vue'
import CityName from './components/CityName.vue'
export default {

  name: 'App',
  components: {
    HeaderTop,
    CityName
  },
  data() {
    return {
      city_population: []
    }
  },
  methods: {
    async fetchPlaces() {
      const res = await fetch("https://webbackend8013.onrender.com/api")
      const data = await res.json()
      console.log(data)
      return data[0].city_population;
    }

  },
  async created() {
    this.city_population = await this.fetchPlaces()
  }

}

</script>


<style >
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}


body {
  font-family: "Montserrat", sans-serif;
}

.container {
  margin: 30px;
  position: absolute;
  top: 80%;
  left: 50%;
  transform: translate(-50%,-50%);
  overflow: auto;
  min-height: 300px;
  border: 0.4em solid black;
  padding: 30px;
  border-radius: 5px;
  color: rgb(15, 1, 1);
  background-color: rgb(207, 218, 157);
  font-size: 15px;
  max-width:900px;
  border-radius: 30px;
}

</style>