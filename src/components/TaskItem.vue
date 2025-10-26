<template>
  <div class="task-card">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
import type { ITask } from './Class'
defineProps<{ task: ITask }>()
</script>

<style scoped>
.task-card {
  border-radius: 10px;
  padding: 14px;
  background: linear-gradient(180deg, #0b1320, #071025);
  border: 1px solid rgba(255,255,255,0.04);
  color: #e6eef8;
  box-shadow: 0 6px 18px rgba(2,6,23,0.6);
}

.edit-form input {
  display: block;
  width: 100%;
  margin-bottom: 8px;
  padding: 10px 12px;
  border-radius: 8px;
  border: 1px solid rgba(255,255,255,0.06);
  background: rgba(255,255,255,0.02);
  color: #e6eef8;
}

.edit-form input::placeholder { color: rgba(230,238,248,0.45); }
</style>