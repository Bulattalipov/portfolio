<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    },
    profession: {
      type: String,
      required: true
    },
    location: {
      type: String,
      required: true
    },
    img: {
      type: String,
      required: true
    },
    date: {
      type: String,
      required: true
    },
    desc: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div class="achievements__item">
    <div class="achievements__item-box">
      <div class="achievements__item-box-top">
        <div class="achievements__item-box-top-date">{{ date }}</div>
        <div class="achievements__item-box-top-location">{{ location }}</div>
      </div>
      <div class="achievements__item-box-holder">
        <img
          class="achievements__item-box-img"
          :src="'assets/img/achievements/' + img"
          :alt="title"
        />
        <div class="achievements__item-box-info">
          <div class="achievements__item-box-info-profession">{{ profession }}</div>
          <div class="achievements__item-box-info-name">{{ name }}</div>
        </div>
      </div>
    </div>
    <p class="achievements__item-text">{{ desc }}</p>
  </div>
</template>

<style scoped lang="scss">
.achievements {
  &__item {
    display: flex;
    gap: 20px;
    padding-left: 40px;
    position: relative;
    padding-top: 5px;
    padding-bottom: 20px;
    overflow: hidden;

    @media screen and (max-width: 575px) {
      flex-direction: column;
      padding-bottom: 25px;
    }

    &::before {
      content: '';
      position: absolute;
      left: 8px;
      top: 8px;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background-color: #2e2e48;
    }

    &::after {
      content: '';
      position: absolute;
      top: 24px;
      left: 11px;
      width: 2px;
      height: 100%;
      background-color: #f7f9fc;
    }
  }

  &__item-box {
    width: 100%;
    max-width: 262px;
  }

  &__item-text {
    letter-spacing: 0.01em;
    color: #79819a;
    width: 100%;
  }

  &__item-box-top {
    display: flex;
    margin-bottom: 8px;
  }

  &__item-box-holder {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  &__item-box-img {
    width: 45px;
    height: 45px;
    object-fit: contain;
  }

  &__item-box-top-date {
    font-size: 10px;
    letter-spacing: 0.01em;
    color: #47516b;
    margin-right: 4px;
  }

  &__item-box-top-location {
    display: flex;
    align-items: center;
    font-size: 10px;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-left: 4px;

    &::before {
      content: '';
      background-image: url('../assets/img/location-mini.svg');
      width: 8px;
      height: 11px;
      margin-right: 3px;
    }
  }

  &__item-box-info-profession {
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 4px;
  }

  &__item-box-info-name {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #2e2e48;
  }
}
</style>
