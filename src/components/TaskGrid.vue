<template>
  <div class="task-grid">
    <template v-if="tasks.length">
      <Task v-for="task in tasks" :key="task.name" :task="task"></Task>
    </template>
    <p v-else>Sua vida esta em dias :)</p>
  </div>
</template>

<script>
import Task from "./Task";
export default {
  components: { Task },
  props: {
    tasks: { type: Array, required: true }
  }
};
</script>

<style>
</style>