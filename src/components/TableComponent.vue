<script>
export default {
  props: ['title', 'columns', 'rows']
}
</script>

<template>
  <h2>{{ title }}</h2>

  <table>
    <thead>
      <tr>
        <th v-for="c in columns" :key="c.key">{{ c.label }}</th>
      </tr>
    </thead>

    <tbody>
      <tr v-for="(row, index) in rows" :key="index">
        <td v-for="c in columns" :key="c.key">{{ row[c.key] }}</td>
      </tr>
    </tbody>
  </table>

  <p v-if="rows.length === 0">Aucune donnée</p>
</template>
