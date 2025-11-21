<template>
  <div class="content-flex">
    <GoodsCom tag="数码">
      <template v-slot:header>
        <img
          class="product-img"
          src="../assets/computer.jpeg"
          alt="笔记本电脑" />
        <h3 class="product-title">笔记本电脑</h3>
        <p class="product-desc">便携性与功能实用性的平衡。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥3999</span>
      </template>
    </GoodsCom>

    <GoodsCom tag="手机">
      <template v-slot:header>
        <img class="product-img" src="../assets/computer.jpeg" alt="智能手机" />
        <h3 class="product-title">智能手机 Pro Max</h3>
        <p class="product-desc">超视网膜XDR显示屏，A16仿生芯片。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥8999</span>
      </template>
    </GoodsCom>

    <GoodsCom tag="运动">
      <template v-slot:header>
        <img class="product-img" src="../assets/wireless.jpg" alt="运动跑鞋" />
        <h3 class="product-title">减震运动跑鞋</h3>
        <p class="product-desc">轻量化设计，透气网面。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥299</span>
      </template>
    </GoodsCom>
  </div>
</template>

<script>
import GoodsCom from './GoodsCom.vue'
export default {
  name: 'AllGoods',
  components: { GoodsCom },
}
</script>

<style scoped>
.content-flex {
  display: flex;
  justify-content: space-evenly;
  flex-wrap: wrap;
}
.product-img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.product-title {
  font-size: 18px;
  margin: 10px 0;
}
.product-desc {
  color: #666;
  font-size: 14px;
  margin-bottom: 15px;
  height: 40px;
  overflow: hidden;
}
.current-price {
  color: red;
  font-size: 16px;
  font-weight: bold;
}
</style>
