<template>
  <SfSection class="tech__table">
    <template #heading>
      <SfHeading :level-heading="levelHeading">
        <template #title>
          <span
            >{{
              tableData.values.length - (tableData.values.length % 10)
            }}+</span
          >
          <span>companies</span>
        </template>
        <template #subtitle>
          <p>{{ tableSectionHeading.subtitle }}.</p>
        </template>
      </SfHeading>
    </template>
    <SfTable class="sf-table--bordered w-4/5 mx-5 my-12">
      <SfTableHeading>
        <SfTableHeader v-for="head in heading" :key="head">{{
          head
        }}</SfTableHeader>
      </SfTableHeading>
      <SfTableRow v-for="{ company, index } in values" :key="index">
        <SfTableData v-for="(companyData, index) in row" :key="index">{{
          companyData
        }}</SfTableData>
      </SfTableRow>
    </SfTable>
  </SfSection>
</template>
<script>
import { SfSection, SfTable } from '@storefront-ui/vue'
import * as data from '../db.json'
export default {
  components: {
    SfSection,
    SfTable
  },
  props: {
    tableData: {
      type: Object,
      required: true
    },
    tableSectionHeading: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      values: data.values,
      heading: data.heading,
      levelHeading: 3
    }
  }
}
</script>
