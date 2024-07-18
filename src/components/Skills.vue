<script>
import SkillsItem from './SkillsItem.vue'
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  components: {
    SkillsItem
  },
  data() {
    return {
      skills1: [
        {
          id: 1,
          imgUrl: 'figma.svg',
          title: 'Figma'
        },
        {
          id: 2,
          imgUrl: 'javascript.svg',
          title: 'JavaScript'
        },
        {
          id: 3,
          imgUrl: 'html.svg',
          title: 'HTML'
        }
      ],
      skills2: [
        {
          id: 1,
          imgUrl: 'css.svg',
          title: 'CSS'
        },
        {
          id: 2,
          imgUrl: 'vue.svg',
          title: 'VUE 3'
        },
        {
          id: 3,
          imgUrl: 'vscode.svg',
          title: 'VSCode'
        },
        {
          id: 4,
          imgUrl: 'github.png',
          title: 'GitHub'
        },
        {
          id: 5,
          imgUrl: 'gulp.svg',
          title: 'Gulp'
        },
        {
          id: 6,
          imgUrl: 'scss.png',
          title: 'SCSS'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="skills development-section">
    <div class="title">{{ this.title }}</div>
    <div class="skills__items">
      <SkillsItem v-for="skill1 in skills1" :key="skill1.id" v-bind="skill1" />
    </div>
    <div class="skills__items skills__items--five">
      <SkillsItem v-for="skill2 in skills2" :key="skill2.id" v-bind="skill2" />
    </div>
  </div>
</template>

<style scoped lang="scss">
.skills {
  &__items {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 8px;

    &:not(:last-child) {
      margin-bottom: 8px;
    }

    &--five {
      grid-template-columns: repeat(5, 1fr);
    }

    @media screen and (max-width: 767px) {
      grid-template-columns: repeat(1, 1fr);
    }
  }
}
</style>
