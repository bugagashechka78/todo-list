<template>
  <n-modal v-model:show="showModal">
    <n-card
        style="width: 600px"
        title="Modal"
        :bordered="false"
        size="huge"
        role="dialog"
        aria-modal="true"
    >
      <n-flex vertical>
        <n-input value="valueTitle" type="text" placeholder="Basic Input" />
        <n-input
            value="valueDescription"
            type="textarea"
            placeholder="Basic Textarea"
        />
      </n-flex>
    </n-card>
  </n-modal>
</template>

<script setup lang="ts">
import {NFlex, NCard, NModal, NInput} from 'naive-ui'

const showModal = defineModel();

</script>

<style scoped>

</style>