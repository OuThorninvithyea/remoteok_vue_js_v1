<script setup>
import footerData from "@/data/homePageFooterData.json"
import PropBtn from "@/components/globalBtns/propBtn.vue";
</script>

<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-info">
        <p>{{ footerData.text }}</p>
        <div class="search-wrapper">
          <input class="nav-search" id="search-footer" :type="footerData.inputType" :placeholder="footerData.inputPlaceholder">
        </div>
        <PropBtn to="/post-job" text="Subscribe" className="btn btn-primary" id="post-button" />
      </div>
    </div>
    <div class="close-footer">{{ footerData.closeIcon }}</div>
    <div class="close-btn">
    </div>
  </footer>
</template>

<style scoped>

</style>