<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      latest: [
        {
          id: 1,
          imgUrl: 'figma.jpg',
          title: 'Alexa Dev Community Landing Page',
          desc: 'Web UI design for alexa developers comunity',
          link: 'https//figma.com'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="latest development-section">
    <div class="title">{{ this.title }}</div>
    <ul class="latest__items">
      <li v-for="item in latest" :key="item.id" class="latest__item">
        <div class="latest__item-inner">
          <div class="latest__item-img">
            <img
              class="latest__item-img-elem"
              :src="'assets/img/latest/' + item.imgUrl"
              alt="Figma"
            />
          </div>
          <div class="latest__item-box">
            <div class="latest__item-title">{{ item.title }}</div>
            <p class="latest__item-desc">{{ item.desc }}</p>
          </div>
        </div>
        <a class="latest__item-link" :href="item.link">
          <div class="latest__item-link-text">{{ item.link }}</div>
        </a>
      </li>
    </ul>
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

  &__item {
    padding: 24px;
    border-radius: 8px;
    background: #f7f9fc;
  }

  &__item-box {
    margin-bottom: 5px;
  }

  &__item-inner {
    display: flex;
    gap: 16px;
  }

  &__item-img {
    position: relative;
    width: 50px;
    height: 50px;
    border-radius: 3px;
    overflow: hidden;
  }

  &__item-img-elem {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  &__item-title {
    font-weight: 500;
    font-size: 16px;
    line-height: 125%;
    color: #2e2e48;
    margin-bottom: 5px;
  }

  &__item-text {
    font-size: 14px;
    line-height: 129%;
    letter-spacing: 0.01em;
    color: #79819a;
  }
}
</style>
