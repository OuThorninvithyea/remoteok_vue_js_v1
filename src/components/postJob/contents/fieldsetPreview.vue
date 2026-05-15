<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.preview
</script>

<template>
    <legend>{{ data.legend }}</legend>
    <div class="preview-info">
        <h2>{{ data.heading }}</h2>
        <p>{{ data.subheading }}</p>
    </div>
    <div class="preview-card">
        <div class="preview-card-header">
            <div class="logo-preview">
                <img :src="data.card.logo" alt="Logo">
                <div class="logo-name">
                    <p>{{ data.card.companyPlaceholder }}</p>
                    <h2>{{ data.card.positionPlaceholder }}</h2>
                    <span class="badge">{{ data.card.locationBadge }}</span>
                </div>
            </div>
            <a href="#" class="btn preview-apply-btn">Apply</a>
        </div>
        <div class="preview-text">
            <h1>{{ data.card.hiringText }}</h1>
            <h2>{{ data.card.roleText }}</h2>
        </div>
        <p>{{ data.card.descriptionPlaceholder }}</p>
        <div class="preview-card box">
            <h1>{{ data.card.applyHeading }}</h1>
            <p>{{ data.card.applyPlaceholder }}</p>
            <a href="#" class="btn preview-apply-btn preview">{{ data.card.applyButtonText }}</a>
        </div>
    </div>
    <div class="water-mark-preview">{{ data.watermark }}</div>
</template>

<style scoped>

</style>