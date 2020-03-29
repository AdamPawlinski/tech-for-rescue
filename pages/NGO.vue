<template>
  <div class="tech__ngo-container">
    <BannerSection :banner="ngoBannerContent" />
    <TableSection
      :table-data="ngoData"
      :tableSectionHeading="ngoTableSectionHeading"
    />
    <FormSection :form="ngoFormInputs" />
  </div>
</template>
<script>
import * as ngoList from '../db.json'
import { BannerSection } from '@/components/BannerSection'
import { TableSection } from '@/components/TableSection'
import { FormSection } from '@/components/FormSection'

export default {
  components: {
    BannerSection,
    TableSection,
    FormSection
  },
  data() {
    return {
      ngoBannerContent: {
        title: 'Helping NGOs get through the COVID-19 crisis',
        description:
          'A voluntary movement connecting IT companies with non-governmental organizations around the world.',
        buttonText: 'I want to volunteer',
        url: '~/assets/images/HERO-IMAGE.svg',
        background: '#FFF'
      },
      ngoData: ngoList,
      ngoTableSectionHeading: {
        title: 'Over 100 companies to help you',
        subtitle:
          'Our list of volounteers equals to over 100 worldwide companies, and is still growing'
      },
      ngoFormInputs: [
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
