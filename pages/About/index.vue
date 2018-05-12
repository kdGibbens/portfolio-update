<template>
  <div class="about">
    <div class="left">
      <div class="card">
        <div class="card__img">
          <img src="https://www.syncron.com/wp-content/uploads/2017/03/img-placeholder.png?x31871" alt="">
        </div>
        <div class="card__info">
          <p>{{name}}</p>
          <p>{{title}}</p>
          <p><a :href="mailTo">{{email}}</a></p>
        </div>
      </div>
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
    export default {
      data() {
        return {
          name: 'Kelly Gibbens',
          title: 'Front-end UI Developer',
          email: 'gibbenskd@gmail.com',
          mailTo: 'mailto:gibbenskd@gmail.com',
          about: {
            title: "Hi, my name is Kelly and I'm a Front-end Developer",
            description: 'About me...'
          }
        }
      }
    }
</script>