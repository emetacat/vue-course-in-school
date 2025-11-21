<template>
  <div class="container">
    <h3><slot name="title"></slot></h3>
    <div>
      <slot name="content"></slot>
      <p><slot name="poster"></slot>， <slot name="time"></slot></p>
    </div>
  </div>
</template>
<script>
export default {}
</script>
<style>
.container {
  width: 300px;
  height: 150px;
  margin: 5px;
  background-color: beige;
  float: left;
}
</style>
