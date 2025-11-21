<template><input :value="modelValue" @input="inputHandler" /></template>
<script>
export default {
  props: ['modelValue'],
  methods: {
    inputHandler(e) {
      //向父组件派发自定义事件update:modelValue
      this.$emit('update:modelValue', e.target.value)
    },
  },
}
</script>
