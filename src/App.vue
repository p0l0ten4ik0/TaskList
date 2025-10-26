<template>
  <div class="app">
    <h1>Список дел</h1>
    <div class="tasks">
      <TaskItem
        v-for="task in tasks"
        :key="task.id"
        :task="task"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { tasksData } from './components/Task'
import type { ITask } from './components/Class'
import TaskItem from './components/TaskItem.vue'

const tasks: ITask[] = tasksData
</script>

<style scoped>
.app {
  padding: 20px;
  font-family: sans-serif;
  max-width: 600px;
  margin: 0 auto;
}

.tasks {
  display: flex;
  flex-direction: column;
  gap: 12px;
}
</style>