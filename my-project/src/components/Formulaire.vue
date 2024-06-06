<template>
  <div>
    <form @submit.prevent="handleSubmit" class="p-4 bg-white rounded shadow-md">
        <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
                Titre
            </label>
            <input type="text" name="title" v-model="fromData.title" class="w-full px-3 py-2 border rounded-md">
        </div>
        <div class="mb-4">
            <label class="block mb-2 text-sm font-bold text-gray-700"> Description:</label>
            <textarea name="description" v-model="fromData.description" class="w-full px-3 py-2 border rounded-md"></textarea>
        </div>
        <div class="mb-4">
            <label class="block mb-2 text-sm font-bold text-gray-700"> Prix:</label>
            <input type="number" name="price" v-model="fromData.price" class="w-full px-3 py-2 border rounded-md">
        </div>
        <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
            Ajouter le produit
        </button>
    </form>
  </div>
</template>

<script>
export default {
    name: 'Formulaire',
    data() {
        return {
            fromData: {
                title: '',
                description: '',
                price: 0
            },
            errors: {}
        }
    },
    methods: {
        handleSubmit(e) {
            console.log(this.fromData);
        }
    },
    props: {
        product: {
            type: Object,
            required: false,
            default: () => ({})
        }
    }
}
</script>
