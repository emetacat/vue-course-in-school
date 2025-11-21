<template>
  <div class="container">
    <!-- 分类组件：监听“分类切换”事件 -->
    <div class="left">
      <CategoryCom @category="categoryHandler" />
    </div>

    <!-- 列表组件：传递筛选后的书籍 -->
    <div class="right">
      <ListCom :books="list" />
    </div>
  </div>
</template>
<script>
import CategoryCom from './components/CategoryCom.vue'
import ListCom from './components/ListCom.vue'
export default {
  components: { CategoryCom, ListCom },
  data() {
    return {
      // 全部书籍数据
      books: [
        { id: 1, name: '鲁迅全集', cid: 1 },
        { id: 2, name: '埃及神话', cid: 1 },
        { id: 3, name: '经济学的诡计', cid: 2 },
        { id: 4, name: '大话中国艺术史', cid: 3 },
        { id: 5, name: '敦煌艺术通识课', cid: 3 },
      ],
      list: [],
    }
  },
  mounted() {
    this.list = this.books.slice()
  },
  components: {
    CategoryCom,
    ListCom,
  },
  methods: {
    // 根据分类id筛选出对应分类的书籍
    categoryHandler(cid) {
      this.list = this.books.filter((book) => book.cid === cid)
    },
  },
}
</script>
<style>
.container {
  overflow: hidden;
  width: 600px;
}
.container .left,
.container .right {
  float: left;
  margin-bottom: -10000px;
  padding-bottom: 10000px;
}
.container .left {
  width: 23%;
  background: rgb(237, 228, 229);
}
.container .right {
  align-content: left;
  width: 77%;
  background: rgb(205, 222, 245);
}
</style>
