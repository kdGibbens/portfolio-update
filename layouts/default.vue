<template>
  <div class="nuxt__container">
    <the-header></the-header>
    <main class="container grid">
      <nuxt/>
      <the-footer></the-footer>
    </main> 
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