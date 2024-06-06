<template>
    <div class="p-6 bg-red-500 text-white flex-grow">
        <li v-for="product in products" :key="product.id">               
                    
            <p>{{ product.title }}</p>
            <p>Prix: {{ product.price }}</p>
            <p>Description: {{ product.description }}</p>
            <p>Images: {{ product.images }}</p> 
        </li>
    </div>
</template>

<script>
export default {
  name: 'ProductList',
  props: {
    products: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
    /*.product-list {
        background-color: #000;
        color: #fff;
        padding: 20px;
        text-align: center;
    }*/
</style>


