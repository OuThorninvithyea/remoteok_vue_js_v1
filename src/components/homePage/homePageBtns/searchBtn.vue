<script setup>
  import searchData from "@/data/dropdown_search_data.json"
</script>

<template>
  <div class="search-wrapper" id="search-dropdown-wrapper">
    <input class="nav-search" id="search-input" type="search" placeholder="🔍 Search ">
    <span class="arrow-down"></span>
    <div class="search-menu" id="search-menu">
      <div class="menu-section">
        <a v-for="item in searchData" :key="item.categoryItem" :href="item.url">
          {{ item.categoryItem }}
        </a>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>