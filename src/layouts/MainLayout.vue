<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-primary">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Ayhanemoon
        </q-toolbar-title>

        <div>App v.1</div>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      Elevated
      class="bg-dark"
    >
      <q-list>
        <q-item-label
          header
          class="text-light"
        >
          Ayhan Samimi
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
          class="text-light"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Linkedin',
    caption: 'See my resume',
    icon: 'fab fa-linkedin',
    link: 'https://www.linkedin.com/in/ayhan-samimi/'
  },
  {
    title: 'Github',
    caption: 'github.com/Ayhanemoon',
    icon: 'code',
    link: 'https://github.com/Ayhanemoon'
  },
  {
    title: 'Telegram',
    caption: 'Send me massage!',
    icon: 'fab fa-telegram',
    link: 'https://telegram.com/ayhanemoon'
  },
  {
    title: 'Instagram',
    caption: '@Ayhanemoon',
    icon: 'fab fa-instagram-square',
    link: 'https://instagram.com/ayhanemoon'
  },
  {
    title: 'Twitter',
    caption: '@Ayhanemoon',
    icon: 'fab fa-twitter-square',
    link: 'https://twitter.com/Ayhanemoon'
  },
  {
    title: 'YouTube',
    caption: '@Ayhanemoon',
    icon: 'fab fa-youtube',
    link: 'https://www.youtube.com/channel/UC02rzltSm1uDU4Ce2E1cdWQ'
  },
  {
    title: 'Website',
    caption: 'Free Online Courses',
    icon: 'favorite',
    link: 'https://icc-aria.ir'
  }
];

import { defineComponent, ref } from 'vue'

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
