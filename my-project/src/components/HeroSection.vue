<template>
    <div class="p-6 bg-green-500 text-white flex-grow">
        <nav>
            <img :src="heroBackgroundImage" alt="Hero Image" class="w-full h-full">
        </nav>
    </div>
</template>

<script>
export default {
  name: 'HeroSection',
  props: {
    heroBackgroundImage: {
      type: String,
      required: true
    }
  }
}
</script>


<style scoped>
/*
    .hero {
        background-color: #914646;
        color: #fff;
        padding: 20px;
        text-align: center;
    }
    */
</style>


