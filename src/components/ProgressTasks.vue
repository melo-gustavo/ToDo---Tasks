<template>
  <div class="progressTask">
    <span class="progress-value">{{ progress }}%</span>
    <div class="progress-bar" :style="{ width: progress + '%' }"></div>
  </div>
</template>

<script>
export default {
  props: {
    progress: {
      type: Number,
      default: 0,
    },
  },
};
</script>

<style scoped>
.progressTask {
  position: relative;
  display: flex;
  background: #fff2;
  height: 22px;
  width: 80%;
  border: 1px solid;
  border-radius: 8px;
  margin: 15px;
  flex-direction: column;
  align-items: center;
}
.progress-bar {
  position: absolute;
  border-radius: 8px;
  height: 100%;
  background: #4CAF50;
  align-self: flex-start;
}
.progress-value {
    z-index: 1; 
}
</style>