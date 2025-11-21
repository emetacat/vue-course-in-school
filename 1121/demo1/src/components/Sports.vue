<template>
  <div class="content-flex">
    <GoodsCom tag="舒适">
      <template v-slot:header>
        <img class="product-img" src="../assets/wireless.jpg" alt="运动跑鞋" />
        <h3 class="product-title">减震运动跑鞋</h3>
        <p class="product-desc">轻量化设计，透气网面，专业缓震鞋底。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥299</span>
        <span class="original-price">¥499</span>
      </template>
    </GoodsCom>

    <GoodsCom>
      <template v-slot:header>
        <img class="product-img" src="../assets/computer.jpeg" alt="运动手表" />
        <h3 class="product-title">智能运动手表</h3>
        <p class="product-desc">心率监测，GPS定位，50米防水，超长续航。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥699</span>
        <span class="original-price">¥899</span>
      </template>
    </GoodsCom>
  </div>
</template>

<script>
import GoodsCom from './GoodsCom.vue'
export default {
  name: 'Sports',
  components: { GoodsCom },
}
</script>

<style scoped></style>
