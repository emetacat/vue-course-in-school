<template>
  <div class="content-flex">
    <GoodsCom tag="舒适">
      <template v-slot:header>
        <img
          class="product-img"
          src="../assets/nike.jpg"
          alt="女子运动鞋骑士鞋" />
        <h3 class="product-title">Air Jordan 4 RM</h3>
        <p class="product-desc">
          多种鞋面元素巧妙融入坚固柔韧的鞋笼中，强韧耐穿，是日常通勤的理想之选。
        </p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥999</span>
        <span class="original-price">¥1099</span>
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
