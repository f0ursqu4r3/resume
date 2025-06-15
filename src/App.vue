<script setup lang="ts">
import { marked } from 'marked'
import { computed } from 'vue'
import 'bulma/css/bulma.css'

import resume from '@/assets/resume.md?raw'

const compiledMarkdown = computed(() => marked.parse(resume))
</script>

<template>
  <div class="resume container is-max-desktop my-5">
    <div class="content" v-html="compiledMarkdown" />
  </div>
</template>
