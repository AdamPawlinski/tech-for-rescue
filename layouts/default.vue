<template>
  <div>
    <sf-header title="IT for the rescue">
      <template #navigation>
        <SfHeaderNavigationItem v-for="item in navigation" :key="item">
          <nuxt-link
            :to="item.link"
            :style="{ display: 'flex', alignItems: 'center', height: '100%' }"
            >{{ item.name }}</nuxt-link
          >
        </SfHeaderNavigationItem>
      </template>
    </sf-header>
    <nuxt />
    <sf-footer />
  </div>
</template>
<script>
import { SfFooter, SfHeader } from '@storefront-ui/vue'
export default {
  components: {
    SfFooter,
    SfHeader
  },
  data() {
    return {
      isMobile: false,
      navigation: [
        { name: 'Idea', link: '/' },
        { name: 'Looking for Help', link: '/LookingForHelp' },
        { name: 'Provide rescue', link: '/ProvifdeRescue' },
        { name: 'Contact', link: '/Contact' }
      ]
    }
  }
}
</script>
<style>
/* @import '@storefront-ui/vue/styles.scss'; */
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
