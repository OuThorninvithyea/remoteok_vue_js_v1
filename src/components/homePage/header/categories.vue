<script setup>
import categoriesData from "@/data/categoriesData.json"
</script>

<template>
  <div class="categories">
    <div class="category-wrapper" id="categories-container">
      <button v-for="filter in categoriesData.filters" :key="filter.label" class="category-button">
        <span class="hover-on-filter">{{ categoriesData.hoverText }}</span> {{ filter.emoji }} {{ filter.label }}
      </button>
    </div>
  </div>
</template>

<style scoped>

</style>