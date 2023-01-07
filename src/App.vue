<template>
  <v-app>
      <v-app-bar elevation="4">
        {{ appTitle }}
      <v-list class="d-flex justify-end" style="width:100%">
        <v-list-tile  v-for="item in menuItems"  :key="item.title">
          <v-icon>{{ item.icon }}</v-icon>
          <v-list-tile-content>{{ item.title }}</v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-app-bar>
    <v-main>
    <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    appTitle: 'Matan&Raz',
      sidebar: false,
      menuItems: [
          { title: 'Home', path: '/home', icon: 'home' },
          { title: 'Sign Up', path: '/', icon: 'face' },
          { title: 'About Us', path: '/', icon: 'info' },
          { title: 'Contact Us', path: '/', icon: 'phone' }
     ]
  }),
}
</script>
