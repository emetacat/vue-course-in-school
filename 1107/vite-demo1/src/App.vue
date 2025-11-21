<template>
  <div>
    <SearchCom />
    <br />
    <VueCard />
    <br />
    <div>
      <button @click="currentTab = 'Tab1'">音乐</button>
      <button @click="currentTab = 'Tab2'">视频</button>
      <button @click="currentTab = 'Tab3'">新闻</button
      ><keep-alive> <component :is="currentTab"></component></keep-alive>
    </div>
  </div>
</template>

<script>
import VueCard from './components/VueCard.vue'
import Tab1 from './components/TabCom1.vue'
import Tab2 from './components/TabCom2.vue'
import Tab3 from './components/TabCom3.vue'
export default {
  data() {
    return {
      currentTab: 'Tab1',
    }
  },
  components: {
    VueCard,
    //注册组件
    Tab1,
    Tab2,
    Tab3,
  },
}
</script>

<style></style>
