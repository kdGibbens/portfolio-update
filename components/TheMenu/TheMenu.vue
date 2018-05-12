<template>
    <div class="menu">
        <nav class="menu__nav nav" v-bind:class="{'open': isOpen}">
                <!--Setup as for loop-->
                <nuxt-link 
                    :to="item.link" 
                    tag="a" 
                    class="nav-item" 
                    v-for="item in navItems" 
                    v-bind:key="item.name">
                        <p v-on:click="closeSideBar">{{ item.name.toUpperCase() }}</p>
                    </nuxt-link >
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
            navItems: {
                home: {
                    name: 'home',
                    link: '/'
                },
                about: {
                    name: 'about',
                    link: '/about'
                },
                portfolio: {
                    name: 'portfolio',
                    link: '/portfolio'
                }
            }
        }
    },
    methods: {
        openSideBar() {
            this.isOpen = !this.isOpen;
        },
        closeSideBar() {
            this.isOpen = false;
            console.log('working');
            
        }
    }
}
</script>
