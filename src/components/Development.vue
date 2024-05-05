<script>
import Achievements from './Achievements.vue'
import Education from './Education.vue'
import Skills from './Skills.vue'
import Latest from './Latest.vue'
import Awards from './Awards.vue'

export default {
  name: 'PortDevelopment',
  components: {
    Achievements,
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
    <Education title="Education"></Education>
    <Achievements title="Achievements"></Achievements>
    <Skills title="Инструменты/Навыки"></Skills>
    <Latest title="Последние проекты"></Latest>
    <Awards title="Сертификаты и награды"></Awards>
  </div>
</template>

<style scoped lang="scss">
.development {
  flex: 1;
  padding: 64px 48px 0 32px;

  @media screen and (max-width: 575px) {
    padding: 32px 24px 0 16px;
  }
}
</style>
