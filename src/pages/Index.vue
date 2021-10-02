<template>
  <q-page class="flex column flex-center">
    <img
      alt="Ayhan Samimi"
      src="~assets/ayhan1.png"
      class="profile"
    >
    <h1 class="text-light">Ayhan Samimi</h1>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'PageIndex'
})
</script>

<style lang="scss" scoped>
.profile {
  width: 250px;
  height: 350px;
  border-radius: 100px;
}

h1{
  font-family: Roboto, -apple-system, BlinkMacSystemFont, 'Segoe UI', Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-weight: 500;
  text-align: center;
}
</style>
