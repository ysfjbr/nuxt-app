<template>
  <div>
    <h1>JOKES1</h1>
    <Joke v-for="joke in jokes" :key="joke.id" :id="joke.id" :joke="joke.joke" />
  </div>
</template>

<script>

import axios from 'axios'
import Joke from '../../components/Joke'

export default {
  
  data () {
    return {
      jokes: []
    }
  },
  head(){
    return{
      title:"JOKES"
    }
  },
  async created () {
    const config = {
      headers: {
         'Accept' : 'application/json'
      }
    }
    const data = await axios.get('https://icanhazdadjoke.com/search',config)
    this.jokes = data.data.results
  }
}
</script>

<style>

</style>
