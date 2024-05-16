<script>
export default {
  props: {
    imgUrl: {
      type: String,
      required: true
    },
    title: {
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
  <div class="skills__item">
    <div class="skills__item-img">
      <img class="skills__item-img-elem" :src="'assets/img/skills/' + imgUrl" :alt="title" />
    </div>
    <div class="skills__item-img-title">{{ title }}</div>
    <div v-if="desc" class="skills__item-img-desc">{{ skill1.desc }}</div>
  </div>
</template>

<style scoped lang="scss">
.skills {
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
