<template>
  <!--<div class="flex flex-col min-h-screen flex-grow">-->
    <div> 
     <h1>About</h1>
    <HeaderNavbar></HeaderNavbar>
     <HeroSection></HeroSection>
     <ProductList></ProductList>
     <MainFooter></MainFooter>
    </div>
  <!--</div>-->

</template>

<script>
import Navbar from '../components/HeaderNavbar.vue';
import Hero from '../components/HeroSection.vue';
import ProductList from '../components/ProductList.vue';
import Footer from '../components/MainFooter.vue';
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


