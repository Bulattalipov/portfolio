<script>
import AchievementsItem from './AchievementsItem.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  components: {
    AchievementsItem
  },
  data() {
    return {
      achievements: [
        {
          id: 1,
          name: 'Alexa Dev Community',
          profession: 'Graphic Designer',
          location: 'Chandigarh',
          img: '2.svg',
          date: 'Oct 2021 - Nov 2021',
          desc: 'Creatively Designing and Developing web UI for Chandigarh University’s Alexa Developer Community, upcoming big launch of full website.'
        },
        {
          id: 2,
          name: 'Winter of Code',
          profession: 'Hacktoberfest Contributor',
          location: 'Online',
          img: '3.svg',
          date: 'Jan 2021 - March 2021',
          desc: 'Overwhelming to be a part of DSC NSEC project - DSC NSEC Algorithms for Winter of Code 2020. First introduction to Git and Github. How github is used by most of the programmers in order to manage the projects.'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="achievements development-section">
    <div class="title">{{ this.title }}</div>
    <div class="achievements__items">
      <AchievementsItem v-for="item in achievements" :key="item.id" v-bind="item" />
    </div>
  </div>
</template>

<style scoped lang="scss"></style>
