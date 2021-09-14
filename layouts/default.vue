<template>
  <v-app dark primary>
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
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
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      <div class="profile-info">
        <v-row>
          <v-toolbar-title class="mr-10" v-text="title" />
          <NuxtLink to="/profile/profileDetail">
          <v-avatar
            color="primary"
            size="35"
          ><img src="@/assets/person.jpg" /></v-avatar>
          </NuxtLink>
        </v-row>
      </div>
      
      
      <v-spacer />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
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
          icon: 'mdi-chart-bubble',
          title: 'Games List',
          to: "/"
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Profile Detail',
          to: "/profile/profileDetail/"
        }
      ],
      title: 'Chopper P.'
    }
  }
}
</script>

<style scoped>
.profile-info {
  margin-left: 70%;
}
</style>
