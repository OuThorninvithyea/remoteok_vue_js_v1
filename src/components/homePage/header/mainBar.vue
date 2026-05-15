<script setup>
import PropBtn from "@/components/globalBtns/propBtn.vue";
import mainBarData from "@/data/mainBarData.json";
</script>

<template>
  <div class="main-bar">
    <div class="bar-container">
      <p>{{ mainBarData.emoji }} {{ mainBarData.text }}
        <a :href="mainBarData.highlightLink" class="highlight-text text-underline bar">{{ mainBarData.highlightText }}</a>
        {{ mainBarData.suffix }}
      </p>
      <div class="bar-container-button">
        <nav class="nav-links">
          <PropBtn to="/post-job" text="Post a remote job →" className="btn btn-primary" id="post-button" />
          <PropBtn to="/" text="Hide this" className="btn btn-secondary" id="post-button" />
        </nav>
      </div>
    </div>
  </div>
</template>

<style scoped>


</style>

