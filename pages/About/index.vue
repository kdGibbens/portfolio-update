<template>
  <div class="about">
    <div class="left">
      <card-info></card-info>
     </div>
    <div class="right">
      <div class="about__text">
        <h3>{{about.title}}</h3>
        <p class="paragraph">
          {{about.description}}
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
            description: 'About me... I do stuff and things'
          }
        }
      },
      components: {
        CardInfo
      }
    }
</script>