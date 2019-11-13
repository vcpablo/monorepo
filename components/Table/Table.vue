<template>
  <table>
    <TableRow
      v-for="(values, index) in items"
      :key="index"
      :values="values"
    />
  </table>
</template>

<script>
import TableRow from '@vcpablo/table-row/TableRow'
export default {
  name: 'JTable',
  props: {
    items: {
      type: Array,
      required: true
    }
  },
  components: {
    TableRow
  }
}
</script>