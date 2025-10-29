<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
    <p>{{ task.date }}</p>
  </div>
</template>

<script setup lang="ts">
import type { ITask } from './Class'
defineProps<{ task: ITask }>()
</script>

<style scoped>
.task-card {
  text-align: center;
  border-radius: 10px;
  padding: 14px;
  background: linear-gradient(180deg, #3f74ca, #084df0);
  border: 1px solid rgba(187, 72, 72, 0.04);
  color: #f5f5f5;
  box-shadow: 0 6px 18px rgba(2,6,23,0.6);
}
</style>