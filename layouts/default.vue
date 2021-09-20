<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      app
      color="blue-grey darken-4"
      disable-resize-watcher
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :href="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      app
      inverted-scroll
      color="blue-grey darken-4"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>
    <v-main>
      <v-container @click="drawer = false">
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      app
      absolute
      color="blue-grey darken-4"
    >
      <span>&copy; {{ `${new Date().getFullYear()} Hegedüs Bálint` }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-apps',
          title: 'About Me',
          to: '/#about-me'
        },
        {
          icon: 'mdi-download-box-outline',
          title: 'Resume',
          to: '/#cv'
        }
      ]
    }
  }
}
</script>

<style>
  html {
    scroll-behavior: smooth;
  }

  .theme--dark.v-application {
    background: none;
  }
</style>
