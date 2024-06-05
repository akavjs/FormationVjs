<template>
    <div class="p-6 bg-blue-500 text-white">
     <Navbar></Navbar>
     <Hero></Hero>
     <ProductList></ProductList>
     <Footer></Footer>
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue';
import Hero from '../components/Hero.vue';
import ProductList from '../components/ProductList.vue';
import Footer from '../components/Footer.vue';
export default {
  name: 'Home',
  components: {
    Navbar,
    Hero,
    ProductList,
    Footer
  }
}
</script>


