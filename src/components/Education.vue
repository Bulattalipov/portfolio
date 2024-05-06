<script>
export default {
  name: 'PortEducation',
  props: {
    title: {
      type: String,
      required: true
    }
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
      <div v-for="item in items" :key="item.id" class="education__item">
        <div class="education__item-box">
          <img
            class="education__item-box-img"
            :src="'assets/img/education/' + item.imgUrl"
            :alt="item.text"
          />
          <div class="education__item-box-text">{{ item.text }}</div>
        </div>
        <div class="education__item-name">{{ item.name }}</div>
        <div class="education__item-date">{{ item.date }}</div>
      </div>
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

  &__item {
    background-color: #f7f9fc;
    padding: 16px 24px 16px 24px;

    &:nth-child(3n + 1) {
      border-radius: 8px 0 0 8px;
    }

    &:nth-child(3n + 3) {
      border-radius: 0 8px 8px 0;
    }
  }

  &__item-box {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 8px;
  }

  &__item-box-img {
    height: 48px;
    max-width: 48px;
  }

  &__item-box-text {
    font-weight: 500;
    font-size: 12px;
    line-height: 133%;
    color: #2e2e48;
  }

  &__item-name {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #2e2e48;
    margin-bottom: 3px;
    -moz-hyphens: auto;
    -webkit-hyphens: auto;
    -ms-hyphens: auto;
  }

  &__item-date {
    font-weight: 400;
    font-size: 10px;
    letter-spacing: 0.01em;
    color: #79819a;
  }
}
</style>
