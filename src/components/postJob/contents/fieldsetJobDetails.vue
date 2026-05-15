<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.jobDetails
const toolbarIcons = formData.toolbarIcons
</script>

<template>
    <legend>{{ data.legend }}</legend>

    <div class="position-details img">
        <label>{{ data.logoUpload.label }}</label>
        <label for="company-logo" class="upload-btn"><span>{{ data.logoUpload.buttonText }}</span></label>
        <input type="file" id="company-logo" class="upload-image">
    </div>

    <div class="position-details">
        <label class="custom-checkbox-container">
            <input type="checkbox" :name="data.brandColor.name" class="hidden-checkbox" :checked="data.brandColor.checked">
            <span class="custom-box"></span>
            <span class="checkbox-text">{{ data.brandColor.text }} <span class="color-swatch"></span></span>
            <span class="btn btn-secondary show-rate">{{ data.brandColor.badge }}</span>
        </label>
    </div>

    <div class="position-details">
        <label>{{ data.salary.label }}</label>
        <div class="salary-range">
            <label>
                <input type="number" :placeholder="data.salary.minPlaceholder" :min="data.salary.min" :max="data.salary.max" :step="data.salary.step" class="position-input minimum-salary" required>
            </label>
            <span class="salary-dash">—</span>
            <label>
                <input type="number" :placeholder="data.salary.maxPlaceholder" :min="data.salary.min" :max="data.salary.max" :step="data.salary.step" class="position-input maximun-salary" required>
            </label>
        </div>
        <p>{{ data.salary.helpText }}</p>
    </div>

    <div class="position-details benefits">
        <label class="tags-job">BENEFITS<span class="tags btn-primary">new</span></label>
        <div class="benefits-container">
            <span v-for="benefit in data.benefits" :key="benefit">{{ benefit }}</span>
        </div>
    </div>

    <div class="job-description-input how-to-apply">
        <label>HOW TO APPLY</label>
        <div class="form-description position-container">
            <div class="form-nav">
                <div v-for="toolbar in toolbarIcons" :key="toolbar.group" :class="toolbar.group">
                    <img v-for="icon in toolbar.icons" :key="icon" class="form-nav-img" :src="icon" :alt="toolbar.group">
                </div>
            </div>
            <label>
                <input class="input-button-form">
            </label>
        </div>
    </div>

    <div class="position-details apply-url">
        <label>{{ data.applyUrl.label }}</label>
        <label>
            <input type="text" :placeholder="data.applyUrl.placeholder" class="position-input" :required="data.applyUrl.required">
        </label>
        <p>{{ data.applyUrl.helpText }}</p>
    </div>

    <div class="position-details apply-email">
        <label>{{ data.applyEmail.label }}</label>
        <label>
            <input type="text" :placeholder="data.applyEmail.placeholder" class="position-input" :required="data.applyEmail.required">
        </label>
        <p>{{ data.applyEmail.helpText }}</p>
    </div>
</template>

<style scoped>

</style>