<script>
import { mapActions, mapState } from 'pinia'
import { useSportStore } from '../src/stores/sport'
import { RouterLink, RouterView } from 'vue-router'

import LoginPage from './views/LoginPage.vue'
import Navbar from './components/Navbar.vue'
import HomePage from './views/HomePage.vue'

export default {
  created() {
    this.fetchFitness()
  },
  data() {
    return {}
  },
  computed: {
    ...mapActions(useSportStore, [''])
  },
  methods: {
    ...mapState(useSportStore, ['loginHandler', 'fetchFitness'])
  },
  components: { LoginPage, Navbar, HomePage }
}
</script>

<template>
  <Navbar />
  <!-- <LoginPage /><HomePage /> -->
  <router-view />
</template>

<style scoped></style>
