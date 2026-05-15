<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.sidebar
</script>

<template>
    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.price.label }}</p>
        <div class="sidebar-stat-value">{{ data.stats.price.value }}</div>
        <p class="sidebar-stat-sub" v-html="data.stats.price.sub"></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.reach.label }}</p>
        <div class="sidebar-stat-value">{{ data.stats.reach.value }}</div>
        <p class="sidebar-stat-sub" v-html="data.stats.reach.sub"></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.rated.label }}</p>
        <div class="sidebar-stat-stars">
            <img v-for="n in data.stats.rated.stars" :key="n" :src="data.stats.rated.starImg" alt="star" class="star full">
        </div>
        <p class="sidebar-stat-sub" v-html="data.stats.rated.sub"></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.emailedTo.label }}</p>
        <div class="sidebar-stat-value">{{ data.stats.emailedTo.value }}</div>
        <p class="sidebar-stat-sub" v-html="data.stats.emailedTo.sub"></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.crosspostedTo.label }}</p>
        <div class="sidebar-stat-value">{{ data.stats.crosspostedTo.value }}</div>
        <p class="sidebar-stat-sub">{{ data.stats.crosspostedTo.sub }} <a :href="data.stats.crosspostedTo.linkUrl" class="sidebar-api-link">{{ data.stats.crosspostedTo.linkText }}</a></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.guaranteed.label }}</p>
        <div class="sidebar-stat-value">{{ data.stats.guaranteed.value }}</div>
        <p class="sidebar-stat-sub" v-html="data.stats.guaranteed.sub"></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.stats.payWith.label }}</p>
        <img :src="data.stats.payWith.payImg" alt="Payment methods" class="pay-logos">
        <p class="sidebar-stat-sub" v-html="data.stats.payWith.sub"></p>
    </div>

    <div class="border-bottom"></div>
    <div class="sidebar-stat">
        <p class="sidebar-stat-label">{{ data.googleStat.label }}</p>
        <div class="sidebar-stat-value sidebar-stat-google">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" class="google-g-icon">
                <path fill="#4285F4" d="M24 9.5c3.54 0 6.71 1.22 9.21 3.6l6.85-6.85C35.9 2.38 30.47 0 24 0 14.62 0 6.51 5.38 2.56 13.22l7.98 6.19C12.43 13.72 17.74 9.5 24 9.5z"/>
                <path fill="#34A853" d="M46.98 24.55c0-1.57-.15-3.09-.38-4.55H24v9.02h12.94c-.58 2.96-2.26 5.48-4.78 7.18l7.73 6c4.51-4.18 7.09-10.36 7.09-17.65z"/>
                <path fill="#FBBC05" d="M10.53 28.59c-.48-1.45-.76-2.99-.76-4.59s.27-3.14.76-4.59l-7.98-6.19C.92 16.46 0 20.12 0 24c0 3.88.92 7.54 2.56 10.78l7.97-6.19z"/>
                <path fill="#EA4335" d="M24 48c6.48 0 11.93-2.13 15.89-5.81l-7.73-6c-2.18 1.48-4.97 2.35-8.16 2.35-6.26 0-11.57-4.22-13.47-9.91l-7.98 6.19C6.51 42.62 14.62 48 24 48z"/>
            </svg>
            {{ data.googleStat.value }}
        </div>
        <p class="sidebar-stat-sub">{{ data.googleStat.sub }}</p>
    </div>
</template>

<style scoped>

</style>