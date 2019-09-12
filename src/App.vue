<template lang="html">
  <div>
    <h1>Beers of BrewDog</h1>
    <div class="main-container">
      <beers-list :beers="beers"></beers-list>
      <beer-detail :beer="selectedBeer"></beer-detail>
      </div>
    </div>
  </template>

  <script>
  import {eventBus} from './main.js'
  import BeerDetail from './components/BeerDetail.vue'
  import BeersList from './components/BeersList.vue'


  export default {
    data(){
      return {
        beers:[],
        selectedBeer: null
      }
    },
    components: {
      "beers-list": BeersList,
      "beer-detail": BeerDetail
    },
    mounted(){
      fetch('https://api.punkapi.com/v2/beers')
      .then(res => res.json())
      .then(beers => this.beers = beers)

      eventBus.$on('beer-selected', (beer) => {
        this.selectedBeer = beer
      })
    }
  }
  </script>

  <style lang="css" scoped>
    .main-container {
      display: flex;
      justify-content: space-between;
      font-family: sans-serif;;
    }

    article {
      border: 2px dashed navy;
      width: 300px;
      height: auto;
      padding: 10px;
      margin-right:50px;
      font-weight: normal;
      border-radius: 10px;
    }
  </style>
