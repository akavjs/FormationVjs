<template>
    <div>
        <HeaderNavbar :links="headerNavLinks" />
        <HeroSection :heroBackgroundImage="heroBackgroundImage" />
        <ProductList :products="products" />
        <MainFooter />
    </div>
</template>

<script>
import HeaderNavbar from '../components/HeaderNavbar.vue';
import HeroSection from '../components/HeroSection.vue';
import ProductList from '../components/ProductList.vue';
import MainFooter from '../components/MainFooter.vue';

import {productsDB} from '../data/productDB.js';
import {mainDB} from '../data/mainDB.js';


export default {
  name: 'HomePage',
  components: {
       HeaderNavbar,
       HeroSection,
       ProductList,
       MainFooter
  },
  data() {
    return {
      products: productsDB.products,
      heroBackgroundImage: mainDB.heroBackgroundImage,
      headerNavLinks: mainDB.headerNavLinks
    };
  },
  methods: {
    handleChildEvent(data) {
      this.childMessage = data;
    }
  }
}

</script>


