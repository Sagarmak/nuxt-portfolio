<template>
  <div class="layout mx-auto bg-background transition duration-300 ease-in-out" :class="{ 'theme-light': lightTheme, 'theme-dark': !lightTheme }">
    <Nav :is-light-theme="lightTheme" @nav-toggle-theme="themeSwitcher" />
    <Nuxt />
  </div>
</template>
<script>
import Nav from "@/components/Nav.vue";
export default {
  components: {
    Nav
  },
  data() {
    return {
      lightTheme: true
    };
  },
  methods: {
    themeSwitcher() {
      this.lightTheme = !this.lightTheme;
    }
  }
}
</script>
<style>
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

header {
  min-height: 10vh;
}

.container {
  width: 90%;
}
</style>
