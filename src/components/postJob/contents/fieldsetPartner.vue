<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.partner
</script>

<template>
    <legend>{{ data.legend }}</legend>
    <div class="health-insurance">
        <div class="logo-insurance">
            <img :src="data.logo" :alt="data.logoAlt">
        </div>
        <div class="job-details logo-title-insurance">
            <h2>{{ data.title }}</h2>
            <p>{{ data.description }}</p>
        </div>
        <a :href="data.buttonLink" class="btn sign-up health">{{ data.buttonText }}</a>
    </div>
</template>

<style scoped>

</style>