<script setup>
const { id } = useRoute().params;
const { data: product } = useFetch(`https://fakestoreapi.com/products/${id}`);
</script>
<template>
  {{ product }}
</template>
