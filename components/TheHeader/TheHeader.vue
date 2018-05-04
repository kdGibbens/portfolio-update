<template>
<div class="container header-container">
    <header class="header">
      <div class="header__logo">
          <h3 class="logo">{{ headerLogo }}</h3>
      </div>
  </header>
</div>
</template>

<script>
    export default {
        name: 'the-header',
        data() {
            return {
                headerLogo: 'kdg',
            }
        }
    }
</script>


