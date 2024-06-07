<template>
  <!--<div class="flex flex-col min-h-screen">-->
  <div>
   <!--<About></About>-->
   <!-- <ChildComponent :message="parentMessage" @child-event="handleChildEvent" /> -->
   <!--<p>Message du composant enfant: {{ childMessage }}</p>-->
   <!--<HomePage />-->
   <router-view />

  </div>
<!--</div>-->
</template>

<script>
//import HomePage from './views/HomePage.vue';


//import ChildComponent from './components/ChildComponent.vue';

export default {
  name: 'App',
 /* components: {
   HomePage 
  },*/
}
</script>

<style>

</style>