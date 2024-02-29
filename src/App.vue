<script>

import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppNavInfo from './components/AppNavInfo.vue';
import AppFooter from './components/AppFooter.vue';

export default{
  components: {
    AppHeader,
    AppContent,
    AppNavInfo,
    AppFooter,

  },
  data(){
    return{

    }
  },
}
</script>

<template>


  
  <AppHeader></AppHeader>

  <AppContent></AppContent>

  <AppNavInfo></AppNavInfo>

  <AppFooter></AppFooter>


 
</template>

<style >


</style>
