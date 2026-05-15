/<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.designPost
</script>

<template>
    <legend>{{ data.legend }}</legend>
    <div class="check-box-post-job">
        <label v-for="item in data.checkboxes" :key="item.name" class="custom-checkbox-container">
            <input type="checkbox" :name="item.name" class="hidden-checkbox" :checked="item.checked">
            <span class="custom-box"></span>
            <span class="checkbox-text">
                {{ item.text }}
                <a v-if="item.linkText" :href="item.linkUrl">{{ item.linkText }}</a>
                <span v-if="item.afterLinkText">{{ item.afterLinkText }}</span>
            </span>
            <span v-if="item.badge" class="btn btn-secondary check-box">{{ item.badge }}</span>
        </label>
        <div class="view-counter">
            <div class="expected-view-counter">
                Expected views <span><label>
                    <input class="position-input" type="text" :placeholder="data.viewCounterPlaceholder">
                </label></span>
            </div>
            <div class="expected-clicks-counter">
                Expected clicks <span><label>
                    <input class="position-input" type="text" :placeholder="data.clicksCounterPlaceholder">
                </label></span>
            </div>
        </div>
    </div>
    <p>{{ data.disclaimer }}</p>
</template>

<style scoped>

</style>