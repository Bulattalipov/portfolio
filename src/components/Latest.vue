<script>
import LatestItem from './LatestItem.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  components: {
    LatestItem
  },
  data() {
    return {
      latest: [
        {
          id: 1,
          imgUrl: 'itmo.jpg',
          title: 'Университет ITMO',
          desc: 'Вёрстка под Bitrix',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, Git, Gulp, Handlebars',
          link: 'https://securityhub.ru/',
          linkGit: 'https://github.com/Bulattalipov/itmo'
        },
        {
          id: 2,
          imgUrl: 'tquality.jpg',
          title: 'Точка Качества',
          desc: 'Вёрстка под Bitrix',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, GitLab, Gulp, Pug, GSAP',
          link: 'https://tquality.ru/',
          linkGit: 'https://github.com/Bulattalipov/tochka-frontend'
        },
        {
          id: 3,
          imgUrl: 'tatsocbank.jpg',
          title: 'Татсоцбанк',
          desc: 'Вёрстка под Bitrix',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, GitLab, Gulp, Pug',
          link: 'https://bulattalipov.github.io/tatsocbank-frontend/',
          linkGit: 'https://github.com/Bulattalipov/tatsocbank-frontend'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="latest development-section">
    <div class="title">{{ this.title }}</div>
    <div class="latest__items">
      <LatestItem v-for="item in latest" :key="item.id" v-bind="item" />
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
