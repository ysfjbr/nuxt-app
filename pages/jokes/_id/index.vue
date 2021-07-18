<template>
<div>
<nuxt-link to="/jokes" >Back To Jokes</nuxt-link >
<h2>{{joke.joke}}</h2>
<hr/>
<small>Joke ID: {{$route.params.id}}</small>
</div>
</template>

<script>
import axios from 'axios'
export default {
    data () {
        return {
            joke:{}
        }
    },
async created () {
    const config = {
      headers: {
         'Accept' : 'application/json'
      }
    }
    const data = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`,config)
    this.joke = data.data
}
}
</script>

<style>
</style>
