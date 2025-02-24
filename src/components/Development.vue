<script>
import AboutMe from './AboutMe.vue'
// import Achievements from './Achievements.vue'
import Education from './Education.vue'
import Skills from './Skills.vue'
import Latest from './Latest.vue'
import Awards from './Awards.vue'

export default {
  components: {
    AboutMe,
    // Achievements,
    Education,
    Skills,
    Latest,
    Awards
  },
  data() {
    return {
      latest: [
        {
          id: 9,
          imgUrl: 'tisbi-nauka.jpg',
          title: 'ТИСБИ Наука',
          desc: 'Вёрстка под Symphony, работа c REST API, подключение графиков',
          stack: 'HTML5, CSS3, SCSS, Javascript, Git, Gulp, Handlebars',
          link: 'https://bulattalipov.github.io/tisbi-nauka/',
          linkGit: 'https://github.com/Bulattalipov/tisbi-nauka'
        },
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
        },
        {
          id: 4,
          imgUrl: 'pkkzn.jpg',
          title: 'Профиль Комплект',
          desc: 'Вёрстка под WordPress',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, GitLab, Gulp',
          link: 'https://pkkzn.ru/',
          linkGit: 'https://github.com/Bulattalipov/profilekit'
        },
        {
          id: 5,
          imgUrl: 'letai.jpg',
          title: 'Летай',
          desc: 'Вёрстка под WordPress',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, GitLab, Gulp, Pug',
          link: 'https://b2b.tattelecom.ru/vats/',
          linkGit: 'https://github.com/Bulattalipov/batc'
        },
        {
          id: 6,
          imgUrl: 'gidrorezka.jpg',
          title: 'Гидрорезка',
          desc: 'Вёрстка под WordPress',
          stack: 'HTML5, CSS3, Javascript, jQuery, GitLab',
          link: 'https://bulattalipov.github.io/gidrorozetka/',
          linkGit: 'https://github.com/Bulattalipov/gidrorozetka'
        },
        {
          id: 7,
          imgUrl: 'bank-kazan.jpg',
          title: 'Банк Казани',
          desc: 'Вёрстка',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, GitLab, Gulp, Pug',
          link: 'https://bulattalipov.github.io/bank-kazan/',
          linkGit: 'https://github.com/Bulattalipov/bank-kazan'
        },
        {
          id: 8,
          imgUrl: 'ramanta.jpg',
          title: 'Раманта',
          desc: 'Вёрстка',
          stack: 'HTML5, CSS3, SCSS, Javascript, jQuery, GitLab, Gulp, Pug, Gsap',
          link: 'https://bulattalipov.github.io/ramanta/',
          linkGit: 'https://github.com/Bulattalipov/ramanta'
        }
      ],
      vueProjects: [
        {
          id: 5,
          imgUrl: 'euphoria.jpg',
          title: 'Euphoria - интернет-магазин одежды',
          desc: 'САЙТ В ПРОЦЕССЕ РАЗРАБОТКИ',
          stack: 'HTML5, CSS3, SCSS, Javascript, Vue 3, Git, Vite, Pinia',
          link: 'https://resonant-chaja-790b95.netlify.app/',
          linkGit: 'https://github.com/Bulattalipov/Euphoria'
        },
        {
          id: 1,
          imgUrl: 'brix.jpg',
          title: 'Brix Templates',
          desc: '',
          stack: 'HTML5, CSS3, SCSS, Javascript, Vue 3, Git, Vite',
          link: 'https://shiny-frangollo-504b47.netlify.app/',
          linkGit: 'https://github.com/Bulattalipov/brix'
        },
        {
          id: 2,
          imgUrl: 'pogoda.jpg',
          title: 'Weather widget',
          desc: '',
          stack: 'HTML5, CSS3, SCSS, Javascript, Vue 3, Git, Vite',
          link: 'https://shiny-frangollo-504b47.netlify.app/',
          linkGit: 'https://github.com/Bulattalipov/weather-widget'
        },
        {
          id: 3,
          imgUrl: 'travalizer.jpg',
          title: 'Travalizer',
          desc: '',
          stack: 'HTML5, CSS3, SCSS, Javascript, Vue 3, Git, Vite',
          link: 'https://golden-llama-e427f0.netlify.app/',
          linkGit: 'https://github.com/Bulattalipov/travalizer'
        },
        {
          id: 4,
          imgUrl: 'files-uploaded.jpg',
          title: 'Files uploaded',
          desc: '',
          stack: 'HTML5, CSS3, SCSS, Javascript, Vue 3, Git, Vite',
          link: 'https://chipper-bombolone-982d3c.netlify.app/',
          linkGit: 'https://github.com/Bulattalipov/uploading-files'
        }
      ]
    }
  }
}
</script>

<template>
  <div class="development">
    <AboutMe title="Обо мне"></AboutMe>
    <Education title="Образование"></Education>
    <!-- <Achievements title="Достижения"></Achievements> -->
    <Skills title="Инструменты/Навыки"></Skills>
    <Latest title="Последние проекты" :list="latest"></Latest>
    <Latest title="Проекты на Vue" :list="vueProjects"></Latest>
    <Awards title="Пройденные курсы"></Awards>
  </div>
</template>

<style scoped lang="scss">
.development {
  max-width: 1100px;
  flex: 1;
  padding: 64px 48px 0 32px;

  @media screen and (max-width: 575px) {
    padding: 32px 24px 0 16px;
  }
}
</style>
