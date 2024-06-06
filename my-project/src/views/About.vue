<template>
  <!--<div class="flex flex-col min-h-screen flex-grow">-->
    <div> 
     <h1>About</h1>
     <Navbar></Navbar>
     <Hero></Hero>
     <ProductList></ProductList>
     <Footer></Footer>
    </div>
  <!--</div>-->

</template>

<script>
import Navbar from '../components/Navbar.vue';
import Hero from '../components/Hero.vue';
import ProductList from '../components/ProductList.vue';
import Footer from '../components/Footer.vue';
export default {
  name: 'About',
  components: {
    Navbar,
    Hero,
    ProductList,
    Footer
  }
}
</script>


