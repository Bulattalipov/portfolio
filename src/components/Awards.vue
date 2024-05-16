<script>
import AwardsItem from './AwardsItem.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  components: {
    AwardsItem
  },
  data() {
    return {
      awards: [
        {
          id: 1,
          imgUrl: 'zerotoone.jpg',
          title: 'От 0 до 1',
          name: 'Курс по верстке',
          date: 'Дек 2021 - Фев 2022'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="awards development-section">
    <div class="title">{{ this.title }}</div>
    <div class="awards__items">
      <AwardsItem v-for="item in awards" :key="item.id" v-bind="item" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.awards {
  &__items {
    margin-left: 24px;
    margin-right: 24px;

    @media screen and (max-width: 991px) {
      margin: 0;
    }
  }
}
</style>
