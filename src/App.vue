<template>
  <div id="app">
    <b-navbar type="dark" variant="primary">
      <!-- Right aligned nav items -->
      <b-navbar-nav class="mr-auto">
        <b-button class="menu-toggle-button" v-b-toggle.sidebar
                  variant="outline-light">
          <b-icon icon="list"></b-icon>
        </b-button>
      </b-navbar-nav>

      <router-link :to="{name: 'Index'}" class="cursor-pointer"
                   tag="b-navbar-brand">
         My Shop Web App 
      </router-link>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
      </b-navbar-nav>
    </b-navbar>

    <Sidebar/>

    <transition mode="out-in" name="fade">
      <router-view></router-view>
    </transition>

  </div>
</template>

<script>
  import Sidebar from './components/layout/Sidebar'

  export default {
    components: {
      Sidebar
    },
    data:()=>({}),

  }
</script>

<style lang="sass">
  @import './assets/css/custom.sass'


</style>
