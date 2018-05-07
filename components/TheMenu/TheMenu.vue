<template>
    <div class="menu">
        <nav class="menu__nav nav">
                <!--Setup as for loop-->
                <nuxt-link to="/" tag="a" class="nav-item">Home</nuxt-link>
                <nuxt-link to="/about" tag="a" class="nav-item">About</nuxt-link>
                <nuxt-link to="/portfolio" tag="a" class="nav-item">Portfolio</nuxt-link>
        </nav>
        <div class="menu__btns">
          <div class="menu__btn--open menu__btn">
              <font-awesome-icon :icon="['fas', 'bars']" />
          </div>
          <div class="menu__btn--close menu__btn">
              <font-awesome-icon :icon="['fas', 'times']" />
          </div>
      </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            
        }
    }
}
    
</script>
