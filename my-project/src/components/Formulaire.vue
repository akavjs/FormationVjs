<template>
  <div>
    <form @submit.prevent="handleSubmit" class="p-4 bg-white rounded shadow-md">
        <div class="mb-4">
            <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
                Titre
            </label>
            <input type="text" name="title" v-model="fromData.title" class="w-full px-3 py-2 border rounded-md">
            <p v-if="errors.title" class="text-red-500 text-sm">{{ errors.title }}</p>
        </div>
        <div class="mb-4">
            <label class="block mb-2 text-sm font-bold text-gray-700"> Description:</label>
            <textarea name="description" v-model="fromData.description" class="w-full px-3 py-2 border rounded-md"></textarea>
            <p v-if="errors.description" class="text-red-500 text-sm">{{ errors.description }}</p>
        </div>
        <div class="mb-4">
            <label class="block mb-2 text-sm font-bold text-gray-700"> Prix:</label>
            <input type="number" name="price" v-model="fromData.price" class="w-full px-3 py-2 border rounded-md">
            <p v-if="errors.price" class="text-red-500 text-sm">{{ errors.price }}</p>
        </div>
        <button type="submit" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
            Ajouter le produit
        </button>
        <p v-if="errors.description" class="text-red-500 text-sm">{{ errors.description }}</p>
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
            errors: {
                title: '',
                description: '',
                price: ''
            }
        }
    },
    methods: {
        validateForm() {
            let formIsValid = true;
            let errors = {};
            if (this.fromData.title) {
                errors.title = 'Le titre est requis';
                formIsValid = false;
            }
            if (!this.fromData.description) {
                errors.description = 'La description est requis';
                formIsValid = false;
            }
            if (!this.fromData.price) {
                errors.price = 'Le prix est requis';
                formIsValid = false;
            } else if (isNoN(this.fromData.price)) {
                errors.price = 'Le prix ne peut pas être négatif';
                formIsValid = false;
            }
            this.errors = errors;
            return formIsValid;
        },
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
