<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list flat>
        <v-list-item-group>
          <v-list-item :nuxt="true" to="/">
            <span>Home</span>
          </v-list-item>

          <v-list-item :nuxt="true" to="/porto">
            <span>Works</span>
          </v-list-item>
        </v-list-item-group>
        <v-divider></v-divider>
        <v-list-item-group>
          <v-list-item target="_blank" href="https://twitter.com/muh_muflih">
            <span>Twitter</span>
          </v-list-item>

          <v-list-item target="_blank" href="https://www.instagram.com/m_muflih5/">
            <span>Instagram</span>
          </v-list-item>

          <v-list-item target="_blank" href="https://www.linkedin.com/in/muhammad-muflih-574b2b71">
            <span>Linkedin</span>
          </v-list-item>

          <v-list-item target="_blank" href="https://github.com//mmuflih55">
            <span>Github</span>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :collapse="collapseOnScroll"
      :collapse-on-scroll="collapseOnScroll"
      fixed
      class="toggle"
    >
      <v-app-bar-nav-icon class="toggle" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <div class="flex-grow-1"></div>
      <!-- <v-input hint="Search..."/>
      <v-btn icon @click="collapseOnScroll=!collapseOnScroll">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>-->
    </v-app-bar>
    <v-app-bar fixed class="nav">
      <v-btn text :nuxt="true" link to="/" active-class="act">Home</v-btn>
      <v-btn text :nuxt="true" link to="/porto">Works</v-btn>
      <v-spacer />
      <v-btn text target="_blank" href="https://twitter.com/muh_muflih">Twitter</v-btn>
      <v-btn text target="_blank" href="https://www.instagram.com/m_muflih5/">Instagram</v-btn>
      <v-btn
        text
        target="_blank"
        href="https://www.linkedin.com/in/muhammad-muflih-574b2b71"
      >Linkedin</v-btn>
      <v-btn text target="_blank" href="https://github.com//mmuflih55">Github</v-btn>
    </v-app-bar>

    <!-- <v-content> -->
    <nuxt />
    <!-- </v-content> -->

    <v-footer :fixed="fixed" app>
      <span>© 2019, By Muhammad Muflih</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      collapseOnScroll: true,
      title: "Vuetify.js"
    };
  }
};
</script>
<style scoped>
@media only screen and (max-width: 600px) {
  .nav {
    display: none;
  }

  .toggle {
    display: block;
  }
}
@media only screen and (min-width: 600px) {
  .nav {
    display: block;
  }

  .toggle {
    display: none;
  }
}

.theme--light.v-btn--active:hover::before,
.theme--light.v-btn--active::before {
  opacity: 0;
}
.v-application .deep-purple--text {
    color: none !important;
}

a {
  text-decoration: none;
  color: black;
}
</style>