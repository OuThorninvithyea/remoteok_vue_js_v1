<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.feedback
</script>

<template>
    <legend>{{ data.legend }}</legend>
    <div class="position-details feed-back">
        <label>{{ data.label }}</label>
        <label>
            <textarea :placeholder="data.placeholder" class="position-input textarea-large"></textarea>
        </label>
        <p>{{ data.helpText }}</p>
    </div>
</template>

<style scoped>

</style>