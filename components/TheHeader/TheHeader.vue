<template>
<div class="header-container">
    <header class="header container">
        <nuxt-link to="/" tag="a" class="header__logo-link">
          <h2 class="header__logo">{{ headerLogo }}</h2>
        </nuxt-link>
      <TheMenu />
  </header>
</div>
</template>

<script>
    import TheMenu from '@/components/TheMenu/TheMenu';
    export default {
        name: 'the-header',
        data() {
            return {
                headerLogo: 'kdg',
            }
        },
        components: {
            TheMenu
        }
    }
</script>


