<script setup>
import formData from '@/data/postjob_form_data.json'
const data = formData.letsStart
const toolbarIcons = formData.toolbarIcons
</script>

<template>
    <legend>{{ data.legend }}</legend>
    <div class="position-details">
      <label>{{ data.position.label }}</label>
      <label>
        <input type="text" :placeholder="data.position.placeholder" class="position-input" :required="data.position.required">
      </label>
      <p>{{ data.position.helpText }}</p>
    </div>
    <div class="company-name-details">
      <label>{{ data.companyName.label }}</label>
      <label>
        <input type="text" :placeholder="data.companyName.placeholder" class="position-input" :required="data.companyName.required">
      </label>
      <p>{{ data.companyName.helpText }}</p>
    </div>
    <div class="job-description-input">
      <label>{{ data.jobDescription.label }} <span class="write-with-ai btn btn-post-primary">{{ data.jobDescription.aiButtonText }}</span>
      </label>
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
    <div class="employee-type-details">
      <label for="employment-type">EMPLOYMENT TYPE*</label>
      <select id="employment-type" class="position-input interactive">
        <option v-for="type in data.employmentTypes" :key="type.value" :value="type.value">{{ type.label }}</option>
      </select>
    </div>
    <div class="primary-tag-details">
      <label for="primary-tag">PRIMARY TAG</label>
      <select id="primary-tag" class="position-input interactive">
        <option v-for="tag in data.primaryTags" :key="tag.value" :value="tag.value" :disabled="tag.disabled" :selected="tag.disabled">{{ tag.label }}</option>
      </select>
      <p>{{ data.primaryTagHelpText }}</p>
    </div>
    <div class="keyword-tags-details">
      <label for="tag-input">{{ data.tags.label }}</label>
      <div class="tag-input-wrapper">
        <div class="tag-selected-list" id="tag-selected-list"></div>
        <input id="tag-input" type="text" :placeholder="data.tags.placeholder" class="position-input tag-search-input" autocomplete="off">
        <ul class="tag-dropdown" id="tag-dropdown"></ul>
      </div>
      <p>{{ data.tags.helpText }}</p>
    </div>
    <div class="job-location-details">
      <label class="tags-job">{{ data.location.label }} <span v-if="data.location.isNew" class="tags btn-primary">new</span></label>
      <label>
        <input type="text" :placeholder="data.location.placeholder" class="position-input" :required="data.location.required">
      </label>
      <p>{{ data.location.helpText }} <span class="job-locations-p highlight-text">{{ data.location.highlightText }}</span>  <span class="text-underline">{{ data.location.underlineText }}</span></p>
    </div>
</template>

<style scoped>

</style>
