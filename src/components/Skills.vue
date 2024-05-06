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
      skills1: [
        {
          id: 1,
          imgUrl: 'figma.png',
          title: 'Figma'
        },
        {
          id: 2,
          imgUrl: 'javascript.png',
          title: 'JavaScript'
        },
        {
          id: 3,
          imgUrl: 'html.png',
          title: 'HTML'
        }
      ],
      skills2: [
        {
          id: 1,
          imgUrl: 'css.png',
          title: 'CSS'
        },
        {
          id: 2,
          imgUrl: 'vue.png',
          title: 'VUE 3'
        },
        {
          id: 3,
          imgUrl: 'vscode.png',
          title: 'VSCode'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="skills development-section">
    <div class="title">{{ this.title }}</div>
    <ul class="skills__items">
      <li v-for="skill1 in skills1" :key="skill1.id" class="skills__item">
        <div class="skills__item-img">
          <img
            class="skills__item-img-elem"
            :src="'assets/img/skills/' + skill1.imgUrl"
            :alt="skill1.title"
          />
        </div>
        <div class="skills__item-img-title">{{ skill1.title }}</div>
        <div v-if="skill1.desc" class="skills__item-img-desc">{{ skill1.desc }}</div>
      </li>
    </ul>
    <ul class="skills__items skills__items--five">
      <li v-for="skill2 in skills2" :key="skill2.id" class="skills__item">
        <div class="skills__item-img">
          <img
            class="skills__item-img-elem"
            :src="'assets/img/skills/' + skill2.imgUrl"
            :alt="skill2.title"
          />
        </div>
        <div class="skills__item-img-title">{{ skill2.title }}</div>
        <div v-if="skill2.desc" class="skills__item-img-desc">{{ skill2.desc }}</div>
      </li>
    </ul>
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
  &__item {
    display: flex;
    flex-direction: column;
    align-items: center;
    border-radius: 8px;
    background: #f7f9fc;
    padding: 20px;

    @media screen and (max-width: 767px) {
      flex-direction: row;
      justify-content: center;
      gap: 20px;
    }
  }

  &__item-img {
    position: relative;
    width: 62px;
    height: 61px;
    margin-bottom: 8px;
    border-radius: 8px;
    overflow: hidden;
  }

  &__item-img-elem {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  &__item-img-title {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #2e2e48;
    margin-bottom: 3px;
  }

  &__item-img-desc {
    font-size: 10px;
    letter-spacing: 0.01em;
    text-align: center;
    color: #79819a;
    text-align: center;
  }
}
</style>
