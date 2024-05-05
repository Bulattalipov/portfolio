<script>
import PortDevelopment from './components/Development.vue'

export default {
  name: 'PortApp',
  components: {
    PortDevelopment
  },
  data() {
    return {}
  }
}
</script>

<template>
  <div class="wrapper">
    <div class="user-info">
      <div class="user-info__img">
        <img class="user-info__img-elem" src="/assets/img/user.jpg" alt="Автор" />
      </div>
      <h1 class="user-info__name">Булат Талипов</h1>
      <p class="user-info__desc">Я Frontend-разработчик</p>
      <ul class="user-info__contacts">
        <li class="user-info__contact">
          <div class="user-info__contact-icon">
            <img class="user-info__contact-icon-elem" src="/assets/img/mail.svg" alt="Почта" />
          </div>
          <div class="user-info__contact-box">
            <div class="user-info__contact-box-title">Email</div>
            <a class="user-info__contact-box-link" href="mailto:bulat0talipov@gmail.com"
              >bulat0talipov@gmail.com</a
            >
          </div>
        </li>
        <!-- <li class="user-info__contact">
            <div class="user-info__contact-icon">
              <img class="user-info__contact-icon-elem" src="/assets/img/link.svg" alt="Ссылка" />
            </div>
            <div class="user-info__contact-box">
              <div class="user-info__contact-box-title">Website</div>
              <a
                class="user-info__contact-box-link"
                href="https://anuragyadav365.github.io/portfolio.html" target="_blank"
                >https://anuragyadav365.github.io/portfolio.html</a
              >
            </div>
          </li> -->
        <li class="user-info__contact">
          <div class="user-info__contact-icon">
            <img class="user-info__contact-icon-elem" src="/assets/img/phone.svg" alt="Телефон" />
          </div>
          <div class="user-info__contact-box">
            <div class="user-info__contact-box-title">Телефон</div>
            <a class="user-info__contact-box-link" href="tel:+79586228194">(+7) 958 622 81 94</a>
          </div>
        </li>
        <li class="user-info__contact">
          <div class="user-info__contact-icon">
            <img
              class="user-info__contact-icon-elem"
              src="/assets/img/location.svg"
              alt="Локация"
            />
          </div>
          <div class="user-info__contact-box">
            <div class="user-info__contact-box-title">Адрес</div>
            <div class="user-info__contact-box-link">Россия, Республика Татарстан, г. Казань</div>
          </div>
        </li>
      </ul>
      <div class="user-info__socials">
        <div class="user-info__socials-title">Социальные</div>
        <ul class="user-info__socials-items">
          <li class="user-info__socials-item">
            <div class="user-info__socials-item-icon">
              <img
                class="user-info__socials-item-icon-elem"
                src="/assets/img/instagram.svg"
                alt="Инстаграм"
              />
            </div>
            <div class="user-info__socials-item-box">
              <div class="user-info__socials-item-box-title">Instagram</div>
              <a
                class="user-info__socials-item-box-link"
                href="https://www.instagram.com/bulat_talipov_?igsh=MXdzc3NubXNpdTQ2cg=="
                >@bulat_talipov_</a
              >
            </div>
          </li>
          <li class="user-info__socials-item">
            <div class="user-info__socials-item-icon">
              <img
                class="user-info__socials-item-icon-elem"
                src="/assets/img/github.svg"
                alt="github"
              />
            </div>
            <div class="user-info__socials-item-box">
              <div class="user-info__socials-item-box-title">Github</div>
              <a class="user-info__socials-item-box-link" href="https://github.com/Bulattalipov"
                >@Bulattalipov</a
              >
            </div>
          </li>
          <!-- <li class="user-info__socials-item">
              <div class="user-info__socials-item-icon">
                <img
                  class="user-info__socials-item-icon-elem"
                  src="/assets/img/twitter.svg"
                  alt="Twitter"
                />
              </div>
              <div class="user-info__socials-item-box">
                <div class="user-info__socials-item-box-title">Twitter</div>
                <a class="user-info__socials-item-box-link" href="https://github.com/AnuragYadav365"
                  >@anuragyadav365</a
                >
              </div>
            </li> -->
          <li class="user-info__socials-item">
            <div class="user-info__socials-item-icon">
              <img
                class="user-info__socials-item-icon-elem"
                src="/assets/img/linkedin.svg"
                alt="Linkedin"
              />
            </div>
            <div class="user-info__socials-item-box">
              <div class="user-info__socials-item-box-title">Linkedin</div>
              <a
                class="user-info__socials-item-box-link"
                href="https://www.linkedin.com/in/%D0%B1%D1%83%D0%BB%D0%B0%D1%82-%D1%82%D0%B0%D0%BB%D0%B8%D0%BF%D0%BE%D0%B2-799ab721a/"
                target="_blank"
                >@Bulattalipov</a
              >
            </div>
          </li>
        </ul>
      </div>
      <div class="user-info__languages">
        <div class="user-info__languages-title">Языки</div>
        <ul class="user-info__languages-items">
          <li class="user-info__languages-item">
            <div class="user-info__languages-item-icon">
              <img
                class="user-info__languages-item-icon-elem"
                src="/assets/img/flag-russia.png"
                alt="Флаг"
              />
            </div>
            <div class="user-info__languages-item-box">
              <div class="user-info__languages-item-box-title">Русский</div>
              <div class="user-info__languages-item-box-text">Очень хорошо</div>
            </div>
          </li>
          <li class="user-info__languages-item">
            <div class="user-info__languages-item-icon">
              <img
                class="user-info__languages-item-icon-elem"
                src="/assets/img/flag-english.svg"
                alt="Флаг"
              />
            </div>
            <div class="user-info__languages-item-box">
              <div class="user-info__languages-item-box-title">English</div>
              <div class="user-info__languages-item-box-text">Elementary</div>
            </div>
          </li>
        </ul>
      </div>
      <div class="user-info__hobbies">
        <div class="user-info__hobbies-title">Хобби и интересы</div>
        <ul class="user-info__hobbies-items">
          <li class="user-info__hobbies-item">
            <img
              class="user-info__hobbies-item-icon"
              src="/assets/img/dumbbell-solid.svg"
              alt="Иконка"
            />
            <div class="user-info__hobbies-item-text">Фитнес</div>
          </li>
          <li class="user-info__hobbies-item">
            <img
              class="user-info__hobbies-item-icon"
              src="/assets/img/person-snowboarding-solid.svg"
              alt="Иконка"
            />
            <div class="user-info__hobbies-item-text">Сноубординг</div>
          </li>
          <li class="user-info__hobbies-item">
            <img
              class="user-info__hobbies-item-icon"
              src="/assets/img/book-solid.svg"
              alt="Иконка"
            />
            <div class="user-info__hobbies-item-text">Чтение</div>
          </li>
        </ul>
      </div>
    </div>
    <PortDevelopment></PortDevelopment>
  </div>
</template>

<style scoped lang="scss">
.wrapper {
  display: flex;

  @media screen and (max-width: 1023px) {
    flex-direction: column;
  }
}

.user-info {
  width: 356px;
  min-height: 100%;
  background-color: #f7f9fc;
  padding: 48.4px;

  @media screen and (max-width: 1023px) {
    width: 100%;
  }

  @media screen and (max-width: 575px) {
    padding: 24px;
  }

  &__img {
    position: relative;
    width: 96px;
    height: 96px;
    flex-shrink: 0;
    border-radius: 50%;
    overflow: hidden;
    margin-bottom: 16px;
  }

  &__img-elem {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &__name {
    font-weight: 500;
    font-size: 32px;
    line-height: 125%;
    letter-spacing: -0.02em;
    color: #2e2e48;
  }

  &__desc {
    font-weight: 500;
    font-size: 18px;
    line-height: 133%;
    letter-spacing: 0.02em;
    color: #47516b;
    margin-top: 32px;
    padding-bottom: 10px;
    border-bottom: 1px solid #e2e6ee;
  }

  &__contacts {
    display: flex;
    flex-direction: column;
    gap: 24px;
    margin-top: 32px;
    padding-bottom: 32px;
    border-bottom: 1px solid #e2e6ee;
    margin-bottom: 32px;

    @media screen and (max-width: 1023px) {
      flex-direction: row;
      gap: 40px;
    }

    @media screen and (max-width: 991px) {
      flex-wrap: wrap;
    }
  }

  &__contact {
    display: flex;
    align-items: center;
    gap: 16px;
  }

  &__contact-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    width: 32px;
    height: 32px;
    background-color: #e2e6ee;
    border-radius: 50%;
  }

  &__contact-icon-elem {
    width: 21px;
    height: 21px;
  }

  &__contact-box-title {
    font-weight: 400;
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 4px;
  }

  &__contact-box-link {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #47516b;
    word-break: break-word;
  }

  &__socials {
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    padding-bottom: 32px;
    border-bottom: 1px solid #e2e6ee;
    margin-bottom: 32px;
  }

  &__socials-items {
    display: flex;
    flex-direction: column;
    gap: 20px;

    @media screen and (max-width: 1023px) {
      flex-direction: row;
      gap: 40px;
    }

    @media screen and (max-width: 991px) {
      flex-wrap: wrap;
    }
  }

  &__socials-title {
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 20px;
  }

  &__socials-item {
    display: flex;
    align-items: center;
  }

  &__socials-item-icon {
    position: relative;
    width: 32px;
    height: 32px;
    margin-right: 16px;
  }

  &__socials-item-icon-elem {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  &__socials-item-box-title {
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 4px;
  }

  &__socials-item-box-link {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    text-decoration: underline;
    text-decoration-skip-ink: none;
    color: #47516b;
  }

  &__languages {
    margin-bottom: 32px;
  }

  &__languages-title {
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 20px;
  }

  &__languages-items {
    display: flex;
    flex-direction: column;
    gap: 20px;

    @media screen and (max-width: 1023px) {
      flex-direction: row;
      gap: 40px;
    }

    @media screen and (max-width: 991px) {
      flex-wrap: wrap;
    }
  }

  &__languages-item {
    display: flex;
    align-items: center;
  }

  &__languages-item-icon {
    position: relative;
    flex-shrink: 0;
    width: 32px;
    height: 24px;
    margin-right: 16px;
  }

  &__languages-item-icon-elem {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }

  &__languages-item-box-title {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #47516b;
    margin-bottom: 4px;
  }

  &__languages-item-box-text {
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
  }

  &__hobbies-title {
    font-size: 12px;
    line-height: 133%;
    letter-spacing: 0.01em;
    color: #79819a;
    margin-bottom: 20px;
  }

  &__hobbies-items {
    display: flex;
    flex-direction: column;
    gap: 20px;

    @media screen and (max-width: 1023px) {
      flex-direction: row;
      gap: 40px;
    }

    @media screen and (max-width: 991px) {
      flex-wrap: wrap;
    }
  }

  &__hobbies-item {
    display: flex;
    align-items: center;
  }

  &__hobbies-item-icon {
    width: 34px;
    height: 34px;
    margin-right: 16px;
  }

  &__hobbies-item-text {
    font-weight: 500;
    font-size: 14px;
    line-height: 129%;
    color: #47516b;
  }
}
</style>
