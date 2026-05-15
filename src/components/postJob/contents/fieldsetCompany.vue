<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.company
</script>

<template>
    <legend>{{ data.legend }}</legend>

    <div v-for="field in data.fields" :key="field.label" class="position-details">
        <label>{{ field.label }}</label>
        <label>
            <textarea v-if="field.type === 'textarea'" :placeholder="field.placeholder" :class="['position-input', field.textareaClass]"></textarea>
            <input v-else :type="field.type" :placeholder="field.placeholder" class="position-input" :required="field.required">
        </label>
        <p>{{ field.helpText }}</p>
    </div>

    <label>{{ data.payLaterLabel }}</label>

    <label class="custom-checkbox-container">
        <input type="checkbox" :name="data.showLogoCheckbox.name" class="hidden-checkbox" :checked="data.showLogoCheckbox.checked">
        <span class="custom-box"></span>
        <span class="checkbox-text">{{ data.showLogoCheckbox.text }}</span>
    </label>
</template>

<style scoped>

</style>