<script>
import TableComponent from './components/TableComponent.vue'

export default {
  components: { TableComponent },

  data() {
    return {
      productColumns: [
        { key: 'name', label: 'Nom' },
        { key: 'price', label: 'Prix (DH)' }
      ],
      products: [
        { name: 'Clavier', price: 150 },
        { name: 'Souris', price: 80 },
        { name: 'Ecran', price: 999 }
      ],

      clientColumns: [
        { key: 'nom', label: 'Nom' },
        { key: 'ville', label: 'Ville' },
        { key: 'tel', label: 'Telephone' }
      ],
      clients: [
        { nom: 'hossam', ville: 'Casablanca', tel: '0600284018' },
        { nom: 'youssef', ville: 'Rabat', tel: '0606060606' }
      ]
    }
  }
}
</script>

<template>
  <header>
    <h1>Table dynamique</h1>
  </header>

  <TableComponent title="Produits" :columns="productColumns" :rows="products" />

  <TableComponent title="Clients" :columns="clientColumns" :rows="clients" />
</template>
