<template>
  <div>
    <a @click="activeCom = 'MusicCom1'" href="#">流行音乐</a><br />
    <a @click="activeCom = 'MusicCom2'" href="#">古典音乐</a><br />
    <a @click="activeCom = 'MusicCom3'" href="#">民族音乐</a><br />
    <component :is="activeCom"></component>
  </div>
</template>
<script>
import MusicCom1 from './MusicCom1.vue'
import MusicCom2 from './MusicCom2.vue'
import MusicCom3 from './MusicCom3.vue'
export default {
  data() {
    return {
      activeCom: 'MusicCom1',
    }
  },
  components: {
    MusicCom1,
    MusicCom2,
    MusicCom3,
  },
}
</script>
<style></style>
