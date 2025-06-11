<template>
  <form @submit.prevent="submitForm">
    <input v-model="name" type="text" placeholder="Nama hewan" required />
    <select v-model="type">
      <option>Anjing</option>
      <option>Kucing</option>
      <option>Kelinci</option>
    </select>
    <button type="submit">Tambah</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      type: 'Anjing'
    }
  },
  methods: {
    submitForm() {
      if (this.name.trim()) {
        this.$emit('add-pet', {
          name: this.name,
          type: this.type
        })
        this.name = ''
        this.type = 'Anjing'
      }
    }
  }
}
</script>

