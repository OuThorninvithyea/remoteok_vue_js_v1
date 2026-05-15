<script setup>
import promoData from "@/data/postjob_promotion_data.json"
const promotion = promoData.promotion
</script>

<template>
  <div class="promotion">
    {{ promotion.icon }} {{ promotion.text }}
  </div>
</template>

<style scoped>

</style>
