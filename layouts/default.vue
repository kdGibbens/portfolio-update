<template>
  <div class="nuxt__container">
    <the-header></the-header>
    <the-menu></the-menu>
    <main class="container grid">
      <nuxt/>
      <the-footer></the-footer>
    </main> 
  </div>
</template>

<script>
  import TheHeader from '@/components/TheHeader/TheHeader';
  import TheMenu from '@/components/TheMenu/TheMenu';
  import TheFooter from '@/components/TheFooter/TheFooter';
  export default {
    components: {
      TheHeader,
      TheMenu,
      TheFooter,
    }
  }
</script>