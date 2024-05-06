<script>
import Development from './components/Development.vue'
import UserInfo from './components/UserInfo.vue'

export default {
  name: 'PortApp',
  components: {
    Development,
    UserInfo
  },
  data() {
    return {}
  }
}
</script>

<template>
  <div class="wrapper">
    <UserInfo></UserInfo>
    <Development></Development>
  </div>
</template>

<style scoped lang="scss">
.wrapper {
  display: flex;

  @media screen and (max-width: 1023px) {
    flex-direction: column;
  }
}
</style>
