<template>
  <div class="content-flex">
    <GoodsCom tag="热销">
      <template v-slot:header>
        <img
          class="product-img"
          src="../assets/computer.jpeg"
          alt="笔记本电脑" />
        <h3 class="product-title">笔记本电脑</h3>
        <p class="product-desc">
          便携性与功能实用性的平衡，能适配多场景使用需求。
        </p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥3999</span>
        <span class="original-price">¥4999</span>
      </template>
    </GoodsCom>

    <GoodsCom tag="新品">
      <template v-slot:header>
        <img
          class="product-img"
          src="../assets/wireless.jpg"
          alt="无线蓝牙耳机" />
        <h3 class="product-title">无线蓝牙耳机</h3>
        <p class="product-desc">高音质，长续航，舒适佩戴体验。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥299</span>
        <span class="original-price">¥399</span>
      </template>
    </GoodsCom>

    <GoodsCom tag="双11">
      <template v-slot:header>
        <img
          class="product-img"
          src="../assets/iphone.jpg"
          alt="iPhone 17 Pro" />
        <h3 class="product-title">iPhone 17 Pro</h3>
        <p class="product-desc">创新设计，打造巅峰性能和超长续航。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥8999</span>
      </template>
    </GoodsCom>

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
