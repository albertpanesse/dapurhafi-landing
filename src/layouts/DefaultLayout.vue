<template>
  <div class="default-layout-wrapper">
    <component :is="ViewComponent" />
    <app-footer></app-footer>
  </div>
</template>

<script>
const NotFound = { template: '<p>Page not found</p>' }

// well, let's define some routes for simple routing logic :)
const routes = {
  '/': Home
}

import Home from '../views/Home'

import { AppFooter } from '../components'

export default {
  name: "default-layout",
  data: function() {
  	return {
    	currentRoute: window.location.pathname  		
  	}
  },
  components: {
    AppFooter
  },
  computed: {
    ViewComponent () {
      return routes[this.currentRoute] || NotFound
    }
  }
}
</script>
