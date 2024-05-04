<script>
// import Achievements from './Achievements.vue'
import Education from './Education.vue'
import Skills from './Skills.vue'
import Latest from './Latest.vue'
import Awards from './Awards.vue'

export default {
  name: 'PortDevelopment',
  components: {
    // Achievements,
    Education,
    Skills,
    Latest,
    Awards
  },
  data() {
    return {}
  }
}
</script>

<template>
  <div class="development">
    <Education></Education>
    <!-- <Achievements></Achievements> -->
    <Skills></Skills>
    <Latest></Latest>
    <Awards></Awards>
  </div>
</template>

<style scoped lang="scss">
.development {
  flex: 1;
  padding: 64px 48px 0 32px;

  @media screen and (max-width: 576px) {
    padding: 32px 24px 0 16px;
  }
}
</style>
