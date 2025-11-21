<template>
  <div>
    <b>书籍列表</b>
    <ul ckass="myul">
      <li v-for="(book, index) in books" :key="book.id">
        <a href="" @click.prevent="clickHandler(book.id)">
          序号：{{ index + 1 }}，书籍名称：{{ book.name }}</a
        >
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: ['books'],
}
</script>
<style scoped>
.myul {
  padding: 0;
  margin: 0;
  text-align: left;
  list-style-type: none;
}
b {
  display: block;
  text-align: center;
}
li {
  list-style-type: none;
}
a {
  text-decoration: none;
}
</style>
