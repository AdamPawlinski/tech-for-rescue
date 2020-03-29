<template>
  <div>
    <SfHeader
      title="IT to the rescue"
      class="sf-header--is-sticky"
      logo="~/assets/images/logo.svg"
    >
      <!-- :wishlist-icon="false"
      :cart-icon="false" -->
      <template #navigation>
        <SfHeaderNavigaionItem v-for="(item, index) in navigation" :key="index">
          <nuxt-link
            :to="item.link"
            :style="{ display: 'flex', alignItems: 'center', height: '100%' }"
            ><SfButton class="sf-button--outline">{{
              item.name
            }}</SfButton></nuxt-link
          >
        </SfHeaderNavigaionItem>
      </template>
      <template #header-icons>
        <SfIcon
          v-for="(icon, index) in headerIcons"
          :key="index"
          :icon="icon"
        />
      </template>
    </SfHeader>
    <nuxt />
    <InformSection />
    <SfFooter :column="1">
      Proudly supported by
      <SfImage :src="src" />
    </SfFooter>
  </div>
</template>
<script>
import '@storefront-ui/vue/styles.scss'
import { SfFooter, SfHeader, SfButton, SfIcon } from '@storefront-ui/vue'
import InformSection from '@/components/InformSection'

export default {
  components: {
    SfFooter,
    SfHeader,
    SfButton,
    SfIcon,
    InformSection
  },
  data() {
    return {
      isMobile: false,
      navigation: [
        { name: 'Home', link: '/' },
        { name: 'Join Us', link: '/LookingForHelp' }
      ],
      src: {
        mobile: {
          url:
            '@assets/images/5e73b0d410e4b4534c046525_Divante_logo_sygnet_dvnt-p-500.png'
        },
        desktop: {
          url:
            '@assets/images/5e73b0d410e4b4534c046525_Divante_logo_sygnet_dvnt-p-500.png'
        }
      },
      headerIcons: [
        '@/assets/images/linkedIn.png',
        '@/assets/images/twitter.png',
        '@/assets/images/facebook.png'
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
