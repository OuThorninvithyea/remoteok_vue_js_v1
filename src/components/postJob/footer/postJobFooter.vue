<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.footer
</script>

<template>
    <footer class="post-job-footer">
        <div class="footer-form-zone">
            <div class="post-job-footer-preview">
                <img :src="data.logo" alt="Logo" class="footer-company-logo">
                <div class="footer-job-info">
                    <p class="footer-company-name">{{ data.companyPlaceholder }}</p>
                    <strong class="footer-position">{{ data.positionPlaceholder }}</strong>
                    <span class="badge footer-badge">{{ data.locationBadge }}</span>
                </div>
                <a href="#" class="btn preview-apply-btn footer-apply-btn">{{ data.applyText }}</a>
            </div>
        </div>
        <div class="footer-sidebar-zone">
            <button class="btn btn-post-primary footer-post-btn">{{ data.postButtonText }}</button>
        </div>
    </footer>
</template>

<style scoped>

</style>