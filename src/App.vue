<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>

    <h2>Parent - {{ carName }}</h2>

    <app-car
            :carName="carName"
            :carYear="carYear"
            :counter="counter"
            @nameChanged="carName = $event"
            @counterUpdated="counter = $event"
    >

    </app-car>

    <app-counter :counter="counter" ></app-counter>

  </div>
</template>

<script>
import Car from './Car.vue'
import Counter from './Counter.vue'

export default {
  name: 'app',
  components: {
    appCar: Car,
    appCounter: Counter
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      carName: "Mers",
      carYear: 2017,
      counter: 0
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
