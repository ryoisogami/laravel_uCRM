<script setup>
import { onMounted } from 'vue';
import Pagination from '@/Components/Pagination'

const props = defineProps({
  customers : Object
})
onMounted(() => { //ページが表示されたタイミングで実行
  console.log(props.customers.last_page);
})
</script>

<template>
  <ul v-for="customer in customers.data" :key="customer.id">
    <li>{{ customer.id }}</li>
    <li>{{ customer.name }}</li>
  </ul>
  <Pagination class="mt-6" :links="customers.links"></Pagination>
</template>