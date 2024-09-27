<template>
  <n-flex justify="space-around" size="large">
    <n-flex vertical>
      <h2>Список дел</h2>
      <n-button size="large" @click="showModal = true">Добавить дело</n-button>
      <n-card
          v-for="todo in todos"
          :title='todo.title'
          :key='todo.id'
      >
        {{ todo.description }}
      </n-card>
    </n-flex>
  </n-flex>
  <TodoModal v-model="showModal"/>
</template>

<script setup lang="ts">
import {ref} from 'vue'
import {NFlex, NCard, NButton} from 'naive-ui'
import TodoModal from '@/components/TodoModal'

const showModal = ref(false);


interface Props {
  todos: [];
}

defineProps<Props>()

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
