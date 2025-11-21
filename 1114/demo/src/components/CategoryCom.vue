<template>
  <div>
    <b>书籍类别</b>
    <ul>
      <li v-for="cate in categories" :key="cate.id">
        <a href="" @click.prevent="clickHandler(cate.id)">{{ cate.name }}</a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      // 定义分类数据
      categories: [
        { id: 1, name: '文学类' },
        { id: 2, name: '经济类' },
        { id: 3, name: '艺术类' },
      ],
    }
  },
  methods: {
    // 点击分类时，向父组件派发事件
    clickHandler(cid) {
      this.$emit('category', cid)
    },
  },
}
</script>
<style scoped>
b {
  display: block;
  text-align: center;
}
ul,
li {
  list-style-type: none;
}
a {
  text-decoration: none;
}
</style>
