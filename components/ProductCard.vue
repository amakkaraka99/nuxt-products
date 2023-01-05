<script setup>
const { product } = defineProps(["product"]);
</script>
<template>
  <div
    class="p-3 rounded-md bg-white shadow-sm hover:shadow-xl h-full text-center"
  >
    <img :src="product.image" alt="product" class="thumb" />
    <p class="font-bold text-gray-500 m-4">
      {{ product.title }}
    </p>
    <p>price: $ {{ product.price }}</p>
    <NuxtLink :to="`product/${product.id}`"
      ><p class="bg-[#12b488] text-white py-2 rounded-md text-sm my-4">
        View Details
      </p>
    </NuxtLink>
  </div>
</template>
<style scoped>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>
