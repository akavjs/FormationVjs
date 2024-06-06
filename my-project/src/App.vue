<template>
  <div class="flex flex-col min-h-screen">
  <div>
   <!--<About></About>-->
   <ChildComponent :message="parentMessage" @child-event="handleChildEvent" />
   <p>Message du composant enfant: {{ childMessage }}</p>

  </div>
</div>
</template>

<script>

import ChildComponent from './components/ChildComponent.vue';

export default {
  name: 'App',
  components: {
      ChildComponent   
  },
  data() {
    return {
      parentMessage: 'Message du parent',
      childMessage: ''
    };
  },
  methods: {
    handleChildEvent(data) {
      this.childMessage = data;
    }
  }
}
</script>

<style>

</style>