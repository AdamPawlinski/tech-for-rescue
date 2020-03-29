<template>
  <SfSection
    class="tech__form"
    :title-heading="formHeading.title"
    :subtitle-heading="formHeading.subtitle"
  >
    <form action="" target="">
      <SfInput v-for="(input, index) in form" :key="index"></SfInput>
      <SfButton type="submit">Submit</SfButton>
    </form>
  </SfSection>
</template>
<script>
import { SfSection, SfInput } from '@storefront-ui/vue'
export default {
  components: {
    SfSection,
    SfInput
  },
  props: {
    formHeading: {
      type: Object,
      required: true
    },
    form: {
      type: Array,
      required: true
    }
  },
  data() {
    return {
      formInputs: [
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        },
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        },
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        },
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        },
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        },
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        },
        {
          value: 'companyName',
          type: 'text',
          label: 'Company Name',
          required: true,
          ariaLabel: 'Company Name'
        }
      ]
    }
  }
}
</script>
