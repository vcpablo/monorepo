<template>
  <table>
     <tr>
      <th
        v-for="(label, index) in header"
        :key="index"
      >
        {{ label }}
      </th>
    </tr>
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
    header: {
      type: Array
    },
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