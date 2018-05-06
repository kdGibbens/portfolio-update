<template>
    <div class="menu">
        <nav class="menu__nav">
            <ul class="nav__list-items">
                <!--Setup as for loop-->
                <nuxt-link to="/" tag="li" class="list-item"><a>Home</a></nuxt-link>
                <nuxt-link to="/about" tag="li" class="list-item"><a>About</a></nuxt-link>
                <nuxt-link to="/portfolio" tag="li" class="list-item"><a>Portfolio</a></nuxt-link>
            </ul>
        </nav>
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
