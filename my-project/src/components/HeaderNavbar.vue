<template>
    <div class="p-6 bg-blue-500 text-white">
        <nav>
            <ul>
                <li v-for="link in links" :key="link.id">
                    <a :href="link.href">{{ link.name }}</a>
                </li>
            </ul>
        </nav>
        
    </div>
    <div>
      <button v-on:click="sayHello">Click me</button>
      <p v-if="showMessage">{{ message }}</p>
    </div>
</template>

<script>
export default {
  name: 'HeaderNavbar',
  data() {
    return {
      showMessage: false,
      message: 'Hello, World!'
    };
  },
  methods: {
    sayHello() {
      this.showMessage = !this.showMessage;
    }
  },
  props: {
    links: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
/*.navbar {
        background-color: #000;
        color: #fff;
        padding: 20px;
        text-align: center;
    }*/
</style>


