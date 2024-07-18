<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true
    },
    text: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    date: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div class="education__item">
    <div class="education__item-box">
      <img class="education__item-box-img" :src="'assets/img/education/' + imgUrl" :alt="text" />
      <div class="education__item-box-text">{{ text }}</div>
    </div>
    <div class="education__item-name">{{ name }}</div>
    <div class="education__item-date">{{ date }}</div>
  </div>
</template>

<style scoped lang="scss">
.education {
  &__item {
    background-color: #f7f9fc;
    padding: 16px 24px 16px 24px;
    border-radius: 8px;
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
