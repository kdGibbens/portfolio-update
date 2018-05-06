<template>
<div class="header-container">
    <header class="header container">
      <div class="header__logo">
          <nuxt-link to="/" tag="div" class="header__logo-link">
              <a><h2 class="logo">{{ headerLogo }}</h2></a>
          </nuxt-link>
      </div>
      <TheMenu />
      <div class="header__menu-btns">
          <div class="menu__btn--open">
              <font-awesome-icon :icon="['fas', 'bars']" />
          </div>
          <div class="menu__btn--close">
              <font-awesome-icon :icon="['fas', 'times']" />
          </div>
      </div>
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


