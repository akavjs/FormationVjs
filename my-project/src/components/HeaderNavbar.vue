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
    <div>
      <button v-on:click="login">Login</button>
      <button v-on:click="logout">Logout</button>
      <p v-if="isLoggedIn">You are logged in</p>
      <p v-else>You are not logged in</p>
    </div>
</template>

<script>
export default {
  name: 'HeaderNavbar',
  data() {
    return {
      showMessage: false,
      message: 'Hello, World!',
      isLoggedIn: false
    };
  },
  methods: {
    sayHello() {
      this.showMessage = !this.showMessage;
    },
    login() {
      this.isLoggedIn = !this.isLoggedIn;
    },
    logout() {
      this.isLoggedIn = false;
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


