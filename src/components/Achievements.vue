<script>
export default {
  name: 'PortAchievements',
  props: {
    title: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      achievements: [
        {
          id: 1,
          name: 'Alexa Dev Community',
          profession: 'Graphic Designer',
          location: 'Chandigarh',
          img: '2.png',
          date: 'Oct 2021 - Nov 2021',
          desc: 'Creatively Designing and Developing web UI for Chandigarh University’s Alexa Developer Community, upcoming big launch of full website.'
        },
        {
          id: 2,
          name: 'Winter of Code',
          profession: 'Hacktoberfest Contributor',
          location: 'Online',
          img: '3.png',
          date: 'Jan 2021 - March 2021',
          desc: 'Overwhelming to be a part of DSC NSEC project - DSC NSEC Algorithms for Winter of Code 2020. First introduction to Git and Github. How github is used by most of the programmers in order to manage the projects.'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="achievements development-section">
    <div class="title">{{ this.title }}</div>
    <ul class="achievements__items">
      <li v-for="item in achievements" :key="item.id" class="achievements__item">
        <div class="achievements__item-box">
          <div class="achievements__item-box-top">
            <div class="achievements__item-box-top-date">{{ item.date }}</div>
            <div class="achievements__item-box-top-location">{{ item.location }}</div>
          </div>
          <div class="achievements__item-box-holder">
            <img
              class="achievements__item-box-img"
              :src="'assets/img/achievements/' + item.img"
              :alt="item.title"
            />
            <div class="achievements__item-box-info">
              <div class="achievements__item-box-info-profession">{{ item.profession }}</div>
              <div class="achievements__item-box-info-name">{{ item.name }}</div>
            </div>
          </div>
        </div>
        <p class="achievements__item-text">{{ item.desc }}</p>
      </li>
    </ul>
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
