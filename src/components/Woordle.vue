<template>
  <table>
    <tr>
      <th v-for="n in 5" v-bind:key="n" :style="{ 'border-right': '1px solid black', 'text-align': 'center' }">
        <input v-model="columns[n - 1]" maxlength="1" size="1" :style="{ 'text-transform': 'uppercase' }">
      </th>
    </tr>
    <tr v-for="(row, index) in rows" :key="index">
      <td v-for="n in 5" v-bind:key="n" :style="{ 'border-right': '1px solid black', 'text-align': 'center' }">
        <input v-model="rows[index][n - 1]" maxlength="1" size="1" :style="{ 'text-transform': 'uppercase' }">
      </td>
    </tr>
  </table>
</template>

<script>
export default {
  data() {
    return {
      rows: [
        [],
        [],
        [],
        [],
        []
      ],
      columns: [
        '',
        '',
        '',
        '',
        ''
      ]
    }
  }
}
</script>
