<template>
  <div>
    <h3>Status Booking</h3>
    <p v-if="pets.length === 0">Belum ada hewan dibooking.</p>
    <p v-else>Total booking: {{ pets.length }}</p>
  </div>
</template>

<script>
export default {
  props: ['pets']
}
</script>