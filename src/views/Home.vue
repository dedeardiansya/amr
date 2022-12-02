<template>
  <div class="home-page" v-if="home" :style="`--bg-image: url(${home.bg_url})`">
    <div class="home-page__wrapper">
      <h1 class="home-page__title">
        {{ home.app_name }} <span aria-hidden="true">{{ home.app_name }}</span>
      </h1>
      <p class="home-page__subtitle mb-5 text-uppercase">{{ home.app_title }}</p>
      <div class="home-page__socials">
        <a v-if="home.fb" :href="home.fb" target="_blank">FACEBOOK</a>
        <a v-if="home.ig" :href="home.ig" target="_blank">INSTAGRAM</a>
        <a v-if="home.gh" :href="home.gh" target="_blank">GITHUB</a>
        <a v-if="home.wa" :href="home.wa" target="_blank">WHATSAPP</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  computed: {
    home() {
      return this.$store.getters.config.home
    }
  }
}
</script>
