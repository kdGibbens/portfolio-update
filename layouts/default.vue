<template>
  <div class="nuxt__container">
    <the-header></the-header>
    <main class="container grid main__content">
      <nuxt/>
    </main> 
    <the-footer></the-footer>
  </div>
</template>

<script>
  import TheHeader from '@/components/TheHeader/TheHeader';
  import TheFooter from '@/components/TheFooter/TheFooter';
  export default {
    components: {
      TheHeader,
      TheFooter,
    }
  }
</script>