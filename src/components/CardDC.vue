        <script>
   export default {
  name: 'CardDC',
  props:{
    comicImg: String,
    comicTitle: String
  }
}
</script>

<template>
<div class="card">
  <div class="card-img">
    <img :src="comicImg" :alt="comicTitle">
  </div>
  
  <span>{{comicTitle}}</span>
</div>
  
</template>
<style lang="scss">
       @use '../styles/partials/variable' as *;
    @use '../styles/partials/mixins' as *;
    .card{
        flex-basis: calc(100% / 6 - 20px);
        display: flex;
        flex-wrap: wrap;
        }
</style>