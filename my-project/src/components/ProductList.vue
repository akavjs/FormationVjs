<template>
  
  <div class="bg-white py-10 sm:py-20">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto mt-16 max-w-2xl rounded-3xl ring-1 ring-gray-200 sm:mt-20 lg:mx-0 lg:flex lg:max-w-none">
          <ul role="list" class="mt-8 grid grid-cols-1 gap-4 text-sm leading-6 text-gray-600 sm:grid-cols-2 sm:gap-6">
            <li v-for="product in products" :key="product.id" class="flex gap-x-3">              
              <div class="p-6 bg-red-500 text-white flex-grow">
                <p>{{ product.title }}</p>
                <p>Prix: ${{ product.price }}</p>
                <p>Description: {{ product.description }}</p>
              </div>
            </li>
          </ul>
        </div>

          </div>
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


