<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.sidebar
</script>

<template>
    <template v-for="testimonial in data.testimonials" :key="testimonial.name">
        <div class="border-bottom"></div>
        <div class="sidebar-stat profile">
            <img :src="testimonial.img" :alt="testimonial.alt">
            <h3>" <span v-if="testimonial.beforeHighlight" class="text-muted">{{ testimonial.beforeHighlight }} </span><span class="text-bg-yellow">{{ testimonial.highlight }}</span><span v-if="testimonial.muted" class="text-muted"> {{ testimonial.muted }}</span></h3>
            <h3>— <span class="text-underline">{{ testimonial.name }}</span>, {{ testimonial.role }} at <span class="text-underline">{{ testimonial.company }}</span></h3>
        </div>
    </template>

    <div class="border-bottom"></div>
    <div class="sidebar-stat profile peter">
        <img :src="data.founder.img" :alt="data.founder.alt">
        <p v-for="paragraph in data.founder.bio" :key="paragraph" class="peter-bio" v-html="paragraph"></p>
        <h3>— <span class="text-underline">{{ data.founder.name }}</span>, {{ data.founder.role }} of <span class="text-underline">{{ data.founder.company }}</span></h3>
    </div>
    <div class="border-bottom"></div>
</template>

<style scoped>

</style>