<script>
import LatestItem from './LatestItem.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    list: {
      type: Object,
      required: true
    }
  },
  components: {
    LatestItem
  }
}
</script>

<template>
  <div class="latest development-section">
    <div class="title">{{ this.title }}</div>
    <div class="latest__items">
      <LatestItem v-for="item in list" :key="item.id" v-bind="item" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.latest {
  &__items {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;

    @media screen and (max-width: 767px) {
      grid-template-columns: repeat(1, 1fr);
    }
  }
}
</style>
