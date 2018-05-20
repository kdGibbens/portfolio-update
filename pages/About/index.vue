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
        <p>{{about.process}}</p>
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
            title: "Hi, my name is Kelly and I build on the Web.",
            description: 'I am passionate about building compelling and engaging web interfaces. I have worked on global campaigns for Tom\'s of Maine, Hill\'s Pet Food and United Rentals, as well as smaller clients looking to have a precesence on the web. I believe in building responsive systems that engage the user and help develop relationships between product owners and with their reach.',
            process: 'I begin development with a mobile approach and grow it out to suit the devices that users are on. Using everything from HTML, CSS, and JavaScript I aim to have the best solutions.'
          }
        }
      },
      components: {
        CardInfo
      }
    }
</script>