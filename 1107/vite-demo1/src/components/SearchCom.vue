<template>
  <div class="search-box">
    <input
      type="text"
      placeholder="搜索"
      v-model="searchText"
      @keyup.enter="handleSearch"
      class="search-input" />
    <button class="search-btn"><FontAwesomeIcon icon="search" />搜索</button>
    <!-- <FontAwesomeIcon icon="search" /> -->
  </div>
</template>
<script>
export default {
  data() {
    return {
      searchText: '',
    }
  },
  methods: {
    handleSearch() {},
  },
}
</script>
<style>
.search-box {
  width: 350px; /* 宽度 */
  padding: 8px; /* 内边距 */
  border: 1px solid #ccc; /* 边框 */
  border-radius: 5px; /* 圆角 */
  font-size: 16px; /* 字体大小 */
}
.search-input {
  border: none;
  width: 200px;
  padding: 6px; /* 内边距 */
}
.search-btn {
  margin-left: 10px;
  border: 1px solid black;
}
</style>
