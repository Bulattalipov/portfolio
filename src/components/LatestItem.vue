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
    },
    link: {
      type: String,
      required: true
    },
    stack: {
      type: String,
      required: true
    },
    linkGit: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div class="latest__item">
    <div class="latest__item-inner">
      <div class="latest__item-img">
        <img class="latest__item-img-elem" :src="'assets/img/latest/' + imgUrl" alt="Figma" />
      </div>
      <div class="latest__item-box">
        <div class="latest__item-title">{{ title }}</div>
        <p class="latest__item-desc">{{ desc }}</p>
        <p class="latest__item-stack">Технологии: {{ stack }}</p>
      </div>
    </div>
    <a class="latest__item-link" :href="link" target="_blank">
      <div class="latest__item-link-icon-wrapper">
        <img class="latest__item-link-icon" src="/assets/img/latest/link-mini.svg" :alt="icon" />
      </div>
      <div class="latest__item-link-text">{{ link }}</div>
    </a>
    <a class="latest__item-link" :href="linkGit" target="_blank">
      <div class="latest__item-link-icon-wrapper">
        <img class="latest__item-link-icon" src="/assets/img/latest/github.svg" :alt="icon" />
      </div>
      <div class="latest__item-link-text">{{ linkGit }}</div>
    </a>
  </div>
</template>

<style scoped lang="scss">
.latest {
  &__item {
    padding: 24px;
    border-radius: 8px;
    background: #f7f9fc;
    border: 1px solid rgba(0, 0, 0, 0.2);
  }

  &__item-box {
    margin-bottom: 5px;
  }

  &__item-inner {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  &__item-img {
    position: relative;
    width: 100%;
    height: 210px;
    border-radius: 3px;
    overflow: hidden;
    flex-shrink: 0;
  }

  &__item-img-elem {
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  &__item-link {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-top: 10px;
  }

  &__item-link-icon-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 24px;
    height: 24px;
    border-radius: 50%;
    padding: 16px;
    background-color: #e1e7fe;
  }

  &__item-link-text {
    font-family: var(--second-family);
    font-weight: 600;
    font-size: 15px;
    line-height: 125%;
    text-decoration: underline;
    text-decoration-skip-ink: none;
    color: #516cf7;
    word-break: break-all;
  }

  &__item-title {
    font-weight: 600;
    font-size: 16px;
    line-height: 125%;
    color: #2e2e48;
    margin-bottom: 5px;
  }

  &__item-desc {
    font-size: 14px;
    font-weight: 400;
    line-height: 129%;
    letter-spacing: 0.01em;
  }

  &__item-stack {
    font-size: 14px;
    font-weight: 400;
    line-height: 129%;
    letter-spacing: 0.01em;
    margin-top: 5px;
    font-style: italic;
  }
}
</style>
