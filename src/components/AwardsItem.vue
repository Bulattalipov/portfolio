<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    imgUrl: {
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
  <div class="awards__item">
    <div class="awards__item-box">
      <div class="awards__item-img">
        <img class="awards__item-img-elem" :src="'assets/img/awards/' + imgUrl" alt="Logo" />
      </div>
      <div class="awards__item-info">
        <div class="awards__item-info-title">{{ title }}</div>
        <div class="awards__item-info-name">{{ name }}</div>
      </div>
    </div>
    <div class="awards__item-date">{{ date }}</div>
  </div>
</template>

<style scoped lang="scss">
.awards {
  &__item {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    border-radius: 8px;
    padding: 15px 23px;
    background-color: #f7f9fc;

    @media screen and (max-width: 575px) {
      flex-direction: column;
    }
  }

  &__item-box {
    display: flex;
    justify-content: start;
    gap: 12px;

    @media screen and (max-width: 411px) {
      flex-direction: column;
    }
  }

  &__item-img {
    position: relative;
    border-radius: 10px;
    width: 43px;
    height: 43px;
    overflow: hidden;
    flex-shrink: 0;
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
    flex-shrink: 0;
    font-size: 11px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #47516b;
    margin-left: 30px;

    @media screen and (max-width: 575px) {
      text-align: end;
    }
  }
}
</style>
