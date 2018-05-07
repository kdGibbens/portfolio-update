<template>
    <div class="menu">
        <nav class="menu__nav nav" v-bind:class="{'open': isOpen}">
                <!--Setup as for loop-->
                <nuxt-link to="/" tag="a" class="nav-item">Home</nuxt-link>
                <nuxt-link to="/about" tag="a" class="nav-item">About</nuxt-link>
                <nuxt-link to="/portfolio" tag="a" class="nav-item">Portfolio</nuxt-link>
        </nav>
        <a class="menu__btns" v-on:click="openSideBar" v-bind:class="{'active': isOpen}">
          <span class="menu__btn--open menu__btn" >
              <font-awesome-icon :icon="['fas', 'bars']" />
          </span>
          <span class="menu__btn--close menu__btn">
              <font-awesome-icon :icon="['fas', 'times']" />
          </span>
      </a>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isOpen: false,
        }
    },
    methods: {
        openSideBar() {
            this.isOpen = !this.isOpen;
        }
    }
}
</script>
