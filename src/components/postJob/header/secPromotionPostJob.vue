<script setup>
import secPromotionData  from "@/data/postjob_promotion_data.json";
const secPromotion = secPromotionData.secPromotion
</script>

<template>
  <div class="sec-promotion">
    {{ secPromotion.icon }} {{ secPromotion.text }}
  </div>
</template>

<style scoped>

</style>
