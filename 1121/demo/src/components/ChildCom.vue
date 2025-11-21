<template>
  <div>
    <h2>按钮</h2>
    <slot></slot>
  </div>
  <hr />
  <div>
    <slot name="header"></slot>
    <slot name="content"></slot>
    <p><slot name="footer"></slot></p>
  </div>
</template>
<script>
export default {}
</script>
