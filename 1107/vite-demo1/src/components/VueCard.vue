<template>
  <div class="colorful-card">
    <div class="card-content">
      <img :src="imageSrc" alt="卡片背景图" class="card-image" />
      <h2 class="card-title">{{ title }}</h2>
      <p class="card-description">{{ description }}</p>
      <button class="card-action" @click="handleAction">{{ acivity }}</button>
    </div>
  </div>
</template>

<script>
import imageSrc from '../assets/photo.jpg'
export default {
  data() {
    return {
      imageSrc: imageSrc,
      title: '风景卡片',
      description: '根据风景图片，简单描述风景内容。',
      acivity: '立即行动',
    }
  },
  methods: {
    handleAction() {},
  },
}
</script>

<style scoped>
.colorful-card {
  width: 100%;
  max-width: 800px;
  border-radius: 8px;
  overflow: hidden;
}
.card-image {
  width: 100%;
  height: 300px;
}
.card-title,
.card-description {
  text-align: left;
}
.card-content {
  background: linear-gradient(to bottom, #4682b4, #2f5496);
  padding: 15px;
  color: white;
}
.card-title {
  font-size: 24px;
  margin-bottom: 12px;
}
.card-description {
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 20px;
}
.card-action {
  background-color: transparent;
  border: 2px solid white;
  color: white;
  padding: 10px;
  border-radius: 4px;
  font-size: 16px;
  cursor: pointer;

  display: flex;
  justify-content: left;
}
</style>
