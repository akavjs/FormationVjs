<template>
    <div class="p-6 bg-yellow-500 text-white">
        <nav>
            <p>{{ footerText }}</p>
        </nav>
    </div>
</template>


<script>
export default {
  name: 'MainFooter',
  props: {
    footerText: {
      type: String,
      required: true
    }
  }
}
</script>

<style scoped>
    /*.footer {
        background-color: #000;
        color: #fff;
        padding: 20px;
        text-align: center;
    }*/
</style>
