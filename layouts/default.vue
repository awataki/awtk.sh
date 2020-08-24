<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      clipped
      app
      width="220px"
      overlay-color="primary"
      :mini-variant="!mini"
      :expand-on-hover="!mini"
    >
      <v-list class="py-0">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.link"
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
      clipped-left
      fixed
      flat
      color="primary"
      class="elevation-1"
      dark
    >
      <v-app-bar-nav-icon v-model="drawer" @click="drawer = !drawer" />
      <h1 class="px-6">
        awtk.sh
      </h1>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      drawer: undefined,
      items: [
        {
          title: 'Profile',
          link: '/',
          icon: 'mdi-account'
        },
        {
          title: 'Services',
          link: '/services',
          icon: 'mdi-application'
        }
      ]
    }
  },
  computed: {
    mini () {
      switch (this.$vuetify.breakpoint.name) {
        case 'xs': return true
        case 'sm': return true
        case 'md': return true
        case 'lg': return false
        case 'xl': return false
      }
    }
  }
}
</script>
