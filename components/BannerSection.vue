<template>
  <SfBanner
    :title="banner.title"
    :description="banner.description"
    :button-text="banner.buttonText"
    :image="banner.url"
    :background="banner.background"
  />
</template>
<script>
import { SfBanner } from '@storefront-ui/vue'
export default {
  components: {
    SfBanner
  },
  props: {
    banner: {
      type: Object,
      required: true
    }
  }
}
</script>
