    <script>
    import AppHeader from './components/AppHeader.vue'
    import AppFooter from './components/AppFooter.vue'
    import ComicsList from './components/ComicsList.vue'
    import ComicCard from './components/ComicCard.vue'
    export default {
      components:{
        AppHeader,
        ComicsList,
        ComicCard,
      
        AppFooter
      }
    }
    </script>
<template lang="">
  <AppHeader></AppHeader>
  <ComicsList></ComicsList>
 
  <AppFooter></AppFooter>
</template>
<style lang="scss">
  @use './styles/generals.scss' as *;
</style>