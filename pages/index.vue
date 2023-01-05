<template>
  <HeroSection />
  <section id="shop">
    <div class="container px-6">
      <h1 class="text-4xl text-center text-blue-700 font-semibold my-8">
        Katalog Produk SMAN 9 Luwu Utara
      </h1>
      <div
        class="grid sm:grid-cols-2 :grid-cols-2 md:grid-cols-3 xl:grid-cols-4 gap-6 md:gap-5"
      >
        <div v-for="p in products" :key="p.id">
          <ProductCard :product="p" />
        </div>
      </div>
    </div>
  </section>
</template>
<script setup>
useHead({
  title: "Dropdown Navbar",
  description: "Dropdown Navbar example built with Flowbite",
  script: [
    {
      src: "https://unpkg.com/@themesberg/flowbite@1.1.1/dist/flowbite.bundle.js",
    },
    {
      src: "https://cdn.tailwindcss.com",
    },
  ],
  bodyAttrs: {
    class: "bg-blue-200",
  },
});

const { data: products } = useFetch("https://fakestoreapi.com/products");
</script>
