<script>
import EducationItem from './EducationItem.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  components: {
    EducationItem
  },
  data() {
    return {
      items: [
        {
          id: 1,
          imgUrl: 'KFU.png',
          text: 'Набережночелнинский институт КФУ',
          name: "Наравление 'Сервис'",
          date: '2015 - 2019'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="education development-section">
    <h2 class="title">{{ this.title }}</h2>
    <div class="education__items">
      <EducationItem v-for="item in items" :key="item.id" v-bind="item" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.education {
  &__items {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;

    @media screen and (max-width: 991px) {
      grid-template-columns: repeat(2, 1fr);
    }

    @media screen and (max-width: 575px) {
      grid-template-columns: repeat(1, 1fr);
    }
  }
}
</style>
