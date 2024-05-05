<script>
export default {
  name: 'PortAwards',
  props: {
    title: {
      type: String,
      required: true
    }
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
    <ul class="awards__items">
      <li v-for="item in this.awards" :key="item.id" class="awards__item">
        <div class="awards__item-box">
          <div class="awards__item-img">
            <img
              class="awards__item-img-elem"
              :src="'assets/img/awards/' + item.imgUrl"
              alt="Logo"
            />
          </div>
          <div class="awards__item-info">
            <div class="awards__item-info-title">{{ item.title }}</div>
            <div class="awards__item-info-name">{{ item.name }}</div>
          </div>
        </div>
        <div class="awards__item-date">{{ item.date }}</div>
      </li>
    </ul>
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

  &__item {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    border-radius: 8px;
    padding: 15px 23px;
    background-color: #f7f9fc;

    @media screen and (max-width: 411px) {
      flex-direction: column;
    }
  }

  &__item-box {
    display: flex;
    justify-content: start;
    align-items: center;
    gap: 12px;
  }

  &__item-img {
    position: relative;
    border-radius: 10px;
    width: 43px;
    height: 43px;
    overflow: hidden;
  }

  &__item-img-elem {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  &__item-info-title {
    font-size: 13px;
    line-height: 129%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 4px;
  }

  &__item-info-name {
    font-weight: 500;
    font-size: 15px;
    line-height: 125%;
    color: #2e2e48;
  }

  &__item-date {
    font-size: 11px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #47516b;

    @media screen and (max-width: 411px) {
      text-align: end;
    }
  }
}
</style>
