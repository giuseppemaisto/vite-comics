    <script>
    import AppHeader from './components/AppHeader.vue'
    import AppFooter from './components/AppFooter.vue'
    import AppContent from './components/AppContent.vue'
    import CardDC from './components/CardDC.vue'
    export default {
      components:{
        AppHeader,
        AppContent,
      
        AppFooter
      }
    }
    </script>
<template lang="">
  <AppHeader></AppHeader>
  <AppContent></AppContent>
  
  <AppFooter></AppFooter>
</template>
<style lang="scss">
  @use './styles/generals.scss' as *;
</style>