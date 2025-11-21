<template>
  <div>
    <h1>父组件</h1>
    <ChildCom>
      <template #default>
        <p><button>立即行动</button></p>
      </template>
      <template #header>
        <h2>待办事项</h2>
      </template>
      <template #content>
        <input type="text" placeholder="请输入新任务" />
      </template>
      <template #footer>
        <button>添加任务</button>
      </template>
    </ChildCom>
    <ChildCom1 v-for="(item, index) in topics" :key="index">
      <!-- #是v-slot:的语法糖 -->
      <template #title>帖子标题: {{ item.title }}</template>
      <template #content>帖子内容: {{ item.content }}</template>
      <!-- 添加代码 -->
      <template #poster>发帖人: {{ item.poster }}</template>
      <template #time>发帖时间: {{ item.time }}</template>
    </ChildCom1>
  </div>
</template>

<script>
import ChildCom from './components/ChildCom.vue'
import ChildCom1 from './components/ChidCom1.vue'
export default {
  data() {
    return {
      topics: [
        {
          title: '我爱 Vue',
          content: 'Vue不愧是前端王者！',
          poster: 'Jim',
          time: '2023-11-16',
        },
        {
          title: '关于具名插槽',
          content: '什么是具名插槽呀？',
          poster: 'Lily',
          time: '2023-12-2',
        },
        {
          title: '组件太棒了',
          content: '超赞的组件化开发！',
          poster: 'Bob',
          time: '2023-12-13',
        },
      ],
    }
  },
  components: {
    ChildCom,
    ChildCom1,
  },
}
</script>

<style scoped></style>
