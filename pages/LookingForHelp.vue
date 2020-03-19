<template>
  <sf-table>
    <SfTableHeading>
      <SfTableHeader v-for="head in heading" :key="head">{{
        head
      }}</SfTableHeader>
    </SfTableHeading>
    <SfTableRow v-for="row in data" :key="row['Company Name']">
      <SfTableData v-for="data in row" :key="data">{{ data }}</SfTableData>
    </SfTableRow>
  </sf-table>
</template>
<script>
import { SfTable } from '@storefront-ui/vue'
import * as data from '../db.json'
export default {
  components: {
    SfTable
  },
  data() {
    return {
      data: data.values,
      heading: data.heading
    }
  }
}
</script>
