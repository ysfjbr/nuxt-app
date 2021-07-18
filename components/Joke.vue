<template>
<nuxt-link :to="'/jokes/'+id">
  <div class="joke">
    {{joke}}
  </div>
  </nuxt-link>
</template>

<script>
export default {
 props: ['id','joke']
}
</script>

<style >
.joke {
    padding:15px;
    margin: 15px 0;
    border: 1px solid #ccc;

}
</style>
