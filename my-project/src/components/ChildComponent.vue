<template>
  <div>
    <p>{{ message }}</p>
    <button @click="emitEvent">Envoyer un message au parent</button>
  </div>
</template>

<script>
export default {
  name: 'ChildComponent',
  props: ['message'],
  methods: {
    emitEvent() {
      this.$emit('child-event', 'Bonjour du composant enfant!');
    }
  }
}
</script>

