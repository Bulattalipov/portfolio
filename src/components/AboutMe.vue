<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  },
  data() {
    return {}
  }
}
</script>

<template>
  <div class="about-me">
    <div class="title">{{ this.title }}</div>
    <div class="about-me__desc">
      Привет! Меня зовут Булат Талипов, и я — frontend-разработчик с опытом работы в создании
      современных и функциональных веб-приложений. Мой путь в разработке начался с увлечения
      веб-технологиями, и с тех пор я стремлюсь создавать качественные и удобные интерфейсы для
      пользователей.
    </div>
    <div class="about-me__subtitle">
      На протяжении своей карьеры я работал с различными технологиями и инструментами, что позволило
      мне развить навыки в следующих областях:
    </div>
    <ul>
      <li>
        <b>- Вёрстка и адаптивный дизайн:</b> Я создаю адаптивные и кроссбраузерные интерфейсы,
        используя HTML5, CSS3 и SCSS. Мой опыт включает вёрстку под различные CMS, такие как Bitrix
        и WordPress.
      </li>
      <li>
        <b>- JavaScript и фреймворки:</b> Я активно использую JavaScript для создания интерактивных
        элементов на страницах. В последние годы я также работал с Vue 3, что позволило мне углубить
        свои знания в разработке SPA (одностраничных приложений).
      </li>
      <li>
        <b>- Работа с API:</b> Я имею опыт интеграции REST API, что позволяет мне создавать
        динамичные приложения, взаимодействующие с сервером.
      </li>
      <li>
        <b>- Инструменты разработки:</b> Я использую Git для контроля версий, а также Gulp для
        автоматизации задач, что значительно ускоряет процесс разработки.
      </li>
    </ul>
    <div class="about-me__theend">
      Я стремлюсь к созданию качественного кода и удобных интерфейсов, которые делают взаимодействие
      с веб-приложениями простым и приятным. Если вы ищете надежного и креативного
      frontend-разработчика, я буду рад обсудить возможное сотрудничество!
    </div>
  </div>
</template>

<style scoped lang="scss">
.about-me {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-bottom: 60px;

  &__desc {
    font-size: 18px;
    font-weight: 500;
    margin-bottom: 10px;
  }

  &__subtitle {
    font-size: 18px;
  }

  ul {
    margin-bottom: 20px;
  }

  li {
    font-size: 16px;
    margin-bottom: 5px;

    b {
      font-weight: 600;
    }
  }

  &__theend {
    font-size: 16px;
  }
}

.title {
  margin-bottom: 15px;
}
</style>
