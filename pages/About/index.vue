<template>
  <div class="about">
    <div class="left section">
      <card-info></card-info>
     </div>
    <div class="right section">
      <div class="about__text">
        <h3>{{about.title}}</h3>
        <p class="paragraph">
          {{about.description}}
        </p>
        <p>
          {{about.description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
  import CardInfo from '@/components/Card/CardInfo';
    export default {
      data() {
        return {
          name: 'Kelly Gibbens',
          title: 'Front-end UI Developer',
          email: 'gibbenskd@gmail.com',
          mailTo: 'mailto:gibbenskd@gmail.com',
          about: {
            title: "Hi, my name is Kelly and I'm a Front-end Developer",
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc placerat, diam vitae fermentum lobortis, nisl nulla accumsan sem, quis maximus erat ex sed purus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Nam lorem lorem, lobortis a tellus et, porttitor fringilla ante. Nunc semper neque et ullamcorper posuere. Maecenas faucibus aliquet elit non tristique. Nunc vestibulum iaculis tortor sit amet auctor. Nulla eu elementum mi.'
          }
        }
      },
      components: {
        CardInfo
      }
    }
</script>