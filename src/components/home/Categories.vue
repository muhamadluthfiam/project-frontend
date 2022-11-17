<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <CategoriesCard
        v-for="category in categories"
        :key="category"
        :title="category.title"
        :count="category.count"
        :image="category.image"
      />
    </div>
  </div>
</template>
<script setup>
import { RouterLink } from "vue-router";
import CategoriesCard from "../CategoriesCard.vue";
import { ref } from "vue";

const categories = ref([
  {
    id: 1,
    title: "Mobile UI Kit",
    count: 732,
    image: "/src/assets/img/categories-1.jpg",
  },
  {
    id: 2,
    title: "Fonts",
    count: 732,
    image: "/src/assets/img/categories-2.jpg",
  },
  {
    id: 3,
    title: "Icon Set",
    count: 732,
    image: "/src/assets/img/categories-3.jpg",
  },
  {
    id: 4,
    title: "Website UI Kit",
    count: 732,
    image: "/src/assets/img/categories-4.jpg",
  },
]);
</script>