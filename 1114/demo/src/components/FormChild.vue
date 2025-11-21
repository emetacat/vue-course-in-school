<template>
  <form @submit.prevent="submitForm">
    <p><input v-model="username" placeholder="请输入用户名" /></p>
    <p><input v-model="password" type="password" placeholder="请输入密码" /></p>
    <button type="submit">提交</button>
  </form>
</template>
<script>
export default {
  data() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm() {
      this.$emit('userinfo', this.username, this.password)
    },
  },
}
</script>
