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
</template>

<script>
export default {
  name: 'HeaderNavbar',
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


