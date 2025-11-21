<template>
  <div class="content-flex">
    <GoodsCom tag="5G">
      <template v-slot:header>
        <img class="product-img" src="../assets/computer.jpeg" alt="智能手机" />
        <h3 class="product-title">智能手机 Pro Max</h3>
        <p class="product-desc">
          超视网膜XDR显示屏，A16仿生芯片，4800万像素主摄。
        </p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥8999</span>
        <span class="original-price">¥9999</span>
      </template>
    </GoodsCom>

    <GoodsCom>
      <template v-slot:header>
        <img
          class="product-img"
          src="../assets/wireless.jpg"
          alt="快充数据线" />
        <h3 class="product-title">Type-C 快充线</h3>
        <p class="product-desc">支持60W快充，尼龙编织材质，耐用防缠绕。</p>
      </template>
      <template v-slot:price>
        <span class="current-price">¥29.9</span>
        <span class="original-price">¥59</span>
      </template>
    </GoodsCom>
  </div>
</template>

<script>
import GoodsCom from './GoodsCom.vue'
export default {
  name: 'Mobile',
  components: { GoodsCom },
}
</script>

<style scoped></style>
