<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.sidebar
</script>

<template>
    <div class="trusted-companies-header">
        {{ data.trustedHeader.text }} <span class="text-underline highlight-text text-marked">{{ data.trustedHeader.highlight }}</span>
        {{ data.trustedHeader.afterText }}
    </div>

    <div class="trusted-companies-logos">
        <img v-for="logo in data.trustedLogos" :key="logo.alt" :src="logo.src" :alt="logo.alt">
        <p>{{ data.showMoreText }}</p>
    </div>
</template>

<style scoped>

</style>