<script setup>
import FlashMessageVue from '@/Components/FlashMessage.vue';
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/vue3';
import FlashMessage from '@/Components/FlashMessage.vue';
import { onMounted } from 'vue';

const props = defineProps({
  customers: Object
})

onMounted(() => {
  console.log(props.customers)
})
</script>
